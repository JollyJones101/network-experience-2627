# OPNsense

OPNsense is de edge firewall/router van jullie groepsomgeving. Ze vormt de grens tussen WAN/opleidingsnetwerk en het interne LAN.

## Verwachtingen

Documenteer:

- WAN- en LAN-interface;
- gateway en DNS;
- DHCP indien gebruikt;
- NAT/port forwards;
- firewallregels;
- VPN-configuratie;
- bewijs dat Proxmox-nodes achter OPNsense zitten;
- risico's van gepubliceerde services.

## Basischecks

- OPNsense is bereikbaar voor beheerders.
- LAN-interface gebruikt de juiste IP-range.
- Proxmox-nodes hebben OPNsense als gateway.
- WAN-bereikbaarheid werkt volgens de afspraken van de docent.
- Er zijn geen rechtstreekse WAN-paden buiten OPNsense.

## Firewall en NAT

Regels moeten doelgericht zijn. Vermijd brede regels zoals `allow any any`, tenzij tijdelijk voor diagnose en expliciet gelogd.

Voor elke regel documenteer je:

- doel;
- bron;
- bestemming;
- poort/protocol;
- reden;
- testresultaat;
- rollback of verwijdermoment indien tijdelijk.

Gebruik [templates/firewall-rule-template.md](templates/firewall-rule-template.md).

## VPN

VPN draait bij voorkeur op OPNsense. WireGuard is aanbevolen; OpenVPN mag indien gemotiveerd. Zie [18-vpn.md](18-vpn.md).

## Niet toegestaan

- OPNsense bypassen.
- Proxmox-nodes rechtstreeks op WAN hangen.
- DHCP aanbieden op verkeerde netwerken.
- Publicatie zonder authenticatie en firewallbeperking.

