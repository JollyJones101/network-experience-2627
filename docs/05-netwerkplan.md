# Netwerkplan

Vul dit document aan met het echte netwerkplan van jullie groep. Gebruik [templates/netwerkplan-template.md](templates/netwerkplan-template.md) als structuur.

## Minimale inhoud

- LAN-subnet;
- gateway;
- DNS;
- DHCP-scope;
- relevante bestaande VPN-range en toegelaten routes;
- Proxmox SDN-zone en VNet;
- VLANs indien gebruikt;
- firewallzones;
- firewallregels;
- beheerinterfaces;
- services;
- diagram;
- testplan.

## Overzicht

| Onderdeel | Waarde |
|---|---|
| Groep | `<GROEP_NUMMER>` |
| LAN-subnet | `<DOOR_DOCENT_BEVESTIGD>` |
| Gateway | `<OPNSENSE_LAN_IP>` |
| DNS | `<DNS_SERVER>` |
| DHCP-scope | `<SCOPE_OF_NIET_GEBRUIKT>` |
| VPN-range | `<VPN_RANGE>` |
| SDN VNet | `<VNET_NAAM_EN_RANGE>` |

## Testplan

Voorzie tests voor:

- LAN-connectiviteit;
- DNS-resolutie;
- internet/WAN-bereikbaarheid volgens afspraken;
- VPN-toegang;
- publicatie van de gekozen service via de bestaande reverse proxy;
- automatiserings- en monitoringpaden;
- Proxmox SDN-connectiviteit;
- toegelaten en geblokkeerd firewallverkeer.
