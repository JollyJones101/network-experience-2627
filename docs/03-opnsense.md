# OPNsense

OPNsense is de bestaande edge firewall/router van jullie groepsomgeving. Ze vormt de grens tussen WAN/opleidingsnetwerk en het interne LAN. Studenten installeren of vervangen ze niet.

## Verwachtingen voor studenten

Documenteer:

- netwerkpad en afhankelijkheden van de eigen services;
- benodigde NAT- of firewallwijzigingen via change request;
- positieve en negatieve toegangstests;
- risico's van gepubliceerde services;
- escalatie wanneer de bestaande platformconfiguratie afwijkt.

## Intakechecks

- Beheer via de bestaande VPN werkt volgens de toegewezen rechten.
- De opgegeven gateway, DNS en servicepaden werken.
- Er zijn geen rechtstreekse WAN-paden buiten OPNsense.
- Afwijkingen worden gemeld; de gedeelde basis wordt niet op eigen initiatief herbouwd.

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

De VPN is al operationeel. Studenten valideren hun toegang en voeren alleen account- of routewijzigingen uit volgens de bestaande procedure.

## Niet toegestaan

- OPNsense bypassen.
- Proxmox-nodes rechtstreeks op WAN hangen.
- DHCP aanbieden op verkeerde netwerken.
- Publicatie zonder authenticatie en firewallbeperking.
