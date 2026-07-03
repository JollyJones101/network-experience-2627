# Proxmox SDN

Elke groep gebruikt Proxmox SDN binnen het eigen Proxmox-cluster.

## Minimale realisatie

- minstens een SDN-zone;
- minstens een VNet;
- minstens twee VM's/containers die het netwerk gebruiken;
- connectiviteitstest;
- firewalldocumentatie.

## Onderscheid tussen netwerklagen

Leg uit:

- onderliggende virtuele bekabeling van de docent;
- LAN achter OPNsense;
- Proxmox SDN-netwerken binnen het cluster.

Gebruik geen complexe EVPN/VXLAN-opzet tenzij dat nodig en verdedigbaar is. Een eenvoudige, begrijpbare SDN-opzet is voldoende.

## Documentatie

| Onderdeel | Waarde |
|---|---|
| Zone | `<ZONE_NAAM>` |
| Type | `<SIMPLE/ANDERS>` |
| VNet | `<VNET_NAAM>` |
| Subnet | `<SUBNET>` |
| Gateway | `<GATEWAY_INDIEN_VAN_TOEPASSING>` |
| Gebruikte VM's/containers | `<LIJST>` |

## Testbewijs

- Ping of servicecheck tussen VM's.
- Route- of IP-configuratie.
- Firewalltest.
- Screenshot of export zonder secrets.

