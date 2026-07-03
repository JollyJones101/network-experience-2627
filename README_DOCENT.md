# Cloning group environments: MAC addresses and unique identity

When cloning a complete **doos-Proxmox** environment, be careful with duplicated MAC addresses and system identities.

The lab architecture uses one nested Proxmox VM per group:

```text
Physical Proxmox cluster
└── Group X doos-Proxmox VM
    ├── OPNsense VM
    │   ├── WAN NIC
    │   └── LAN NIC
    ├── Proxmox node 1 VM
    ├── Proxmox node 2 VM
    └── Proxmox node 3 VM
```

When the entire doos-Proxmox VM is cloned, the inner VMs inside that doos may keep the same virtual NIC MAC addresses. This can cause serious network issues if multiple cloned group environments run at the same time.

## Why this matters

Duplicate MAC addresses can cause:

* DHCP leases being assigned incorrectly;
* DHCP reservations matching the wrong group;
* ARP table confusion;
* traffic being sent to the wrong OPNsense instance;
* unstable or unpredictable connectivity;
* multiple groups appearing as the same device to the upstream router or DHCP server.

The most important MAC address is the **OPNsense WAN NIC**, because this is visible on the classroom/WAN network.

## MAC addresses that must be unique per group

At minimum, regenerate or verify the MAC addresses for:

```text
OPNsense WAN NIC
OPNsense LAN NIC
Proxmox node 1 NIC
Proxmox node 2 NIC
Proxmox node 3 NIC
```

The OPNsense WAN MAC is especially important if DHCP reservations are used.

## Recommended cloning workflow

Use this workflow when creating a new group environment:

```text
1. Clone the golden doos-Proxmox VM.
2. Start only the cloned doos-Proxmox VM.
3. Inside the cloned doos-Proxmox, regenerate the MAC addresses of the inner VMs:
   - OPNsense WAN NIC
   - OPNsense LAN NIC
   - Proxmox node 1 NIC
   - Proxmox node 2 NIC
   - Proxmox node 3 NIC
4. Rename the inner Proxmox nodes for the group.
5. Assign or verify the correct IP addresses.
6. Configure the DHCP reservation for the new OPNsense WAN MAC.
7. Boot OPNsense and verify WAN/LAN assignment.
8. Boot the three Proxmox nodes.
9. Create a clean snapshot for the group.
10. Give students access.
```

## Regenerating MAC addresses in the Proxmox GUI

Inside the cloned doos-Proxmox:

```text
VM → Hardware → Network Device → Edit
→ MAC address → Generate
```

Do this for each network device of the inner VMs.

After changing MAC addresses, fully stop and start the affected VMs. A simple reboot is not always enough.

## Regenerating MAC addresses with the CLI

For OPNsense, remove and recreate the NICs while keeping the correct bridges:

```bash
qm set <OPNSENSE_VMID> --delete net0
qm set <OPNSENSE_VMID> --delete net1

qm set <OPNSENSE_VMID> --net0 virtio,bridge=vmbr1
qm set <OPNSENSE_VMID> --net1 virtio,bridge=vmbr2
```

Expected bridge mapping:

```text
OPNsense net0 → vmbr1 → WAN
OPNsense net1 → vmbr2 → LAN
```

For the three nested Proxmox nodes:

```bash
qm set <PVE1_VMID> --delete net0
qm set <PVE1_VMID> --net0 virtio,bridge=vmbr2

qm set <PVE2_VMID> --delete net0
qm set <PVE2_VMID> --net0 virtio,bridge=vmbr2

qm set <PVE3_VMID> --delete net0
qm set <PVE3_VMID> --net0 virtio,bridge=vmbr2
```

Expected bridge mapping:

```text
pve-x-01 net0 → vmbr2 → LAN behind OPNsense
pve-x-02 net0 → vmbr2 → LAN behind OPNsense
pve-x-03 net0 → vmbr2 → LAN behind OPNsense
```

## OPNsense interface assignment after MAC changes

After changing MAC addresses, OPNsense usually keeps the same interface names, such as:

```text
vtnet0
vtnet1
```

However, always verify the interface assignment from the OPNsense console:

```text
1) Assign interfaces
```

Recommended assignment:

```text
WAN = vtnet0
LAN = vtnet1
```

If WAN and LAN are swapped, fix this before giving the environment to students.

## DHCP reservations

If OPNsense WAN uses DHCP, configure a DHCP reservation on the upstream router or classroom DHCP server.

Example:

```text
Group 1 OPNsense WAN MAC → 10.101.0.2
Group 2 OPNsense WAN MAC → 10.102.0.2
Group 3 OPNsense WAN MAC → 10.103.0.2
```

Do not create DHCP reservations based on the MAC address from the golden template. Always use the regenerated MAC address from the cloned group environment.

## Other identities to change after cloning

MAC addresses are not the only duplicated identity. Also check and change:

```text
Hostnames
Static IP addresses
Proxmox node names
SSH host keys, if full uniqueness is required
machine-id on Linux systems, if cloned after installation
```

For this lab, the minimum required changes are:

```text
Unique MAC addresses
Unique hostnames
Unique IP addresses
Correct OPNsense WAN DHCP reservation
```

## Final pre-student checklist

Before handing the environment to a group, verify:

```text
[ ] OPNsense WAN MAC is unique
[ ] OPNsense LAN MAC is unique
[ ] Proxmox node 1 MAC is unique
[ ] Proxmox node 2 MAC is unique
[ ] Proxmox node 3 MAC is unique
[ ] OPNsense WAN receives the correct IP
[ ] OPNsense LAN has the correct group subnet
[ ] WAN and LAN are not swapped
[ ] Proxmox nodes are only connected to the LAN bridge
[ ] No Proxmox node has a direct WAN connection
[ ] Hostnames are unique for the group
[ ] IP addresses are unique for the group
[ ] DHCP reservation uses the regenerated OPNsense WAN MAC
[ ] A clean starting snapshot exists
```

Do not run multiple cloned group environments at the same time until these checks are complete.
