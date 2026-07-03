# Proxmox firewall en security groups

Naast OPNsense gebruiken jullie ook de Proxmox-firewall.

## Verwachtingen

- Proxmox firewall wordt geactiveerd waar passend.
- Security groups worden gebruikt.
- IP sets worden gebruikt waar zinvol.
- Regels worden toegepast op cluster-, node- of VM-niveau waar passend.
- Toegelaten en geblokkeerd verkeer wordt getest.

## Verschil tussen firewalls

| Laag | Doel |
|---|---|
| OPNsense firewall | Edge filtering, NAT, VPN, publicatie |
| Proxmox firewall | Segmentatie en bescherming rond nodes/VM's |
| VM/container firewall | Applicatie- of hostspecifieke filtering |

## Minimaal documenteren

- management access;
- webshare access;
- n8n access;
- inter-VM traffic;
- monitoring traffic;
- backup traffic indien van toepassing.

Gebruik [templates/firewall-security-group-template.md](templates/firewall-security-group-template.md).

