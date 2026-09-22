# Netwerk- en dataflowplan

Vul dit document aan met de echte waarden van de groep. Gebruik het [netwerkplantemplate](templates/netwerkplan-template.md) als start.

## Platformgegevens

| Onderdeel | Waarde |
|---|---|
| Proxmox-pool | `<POOL>` |
| Bridge/VLAN | `<DOOR_DOCENT>` |
| Subnet/gateway | `<DOOR_DOCENT>` |
| DNS/NTP | `<DOOR_DOCENT>` |
| Beheerpad | `<CAMPUS_VPN_OF_ANDERS>` |
| Publicatiepad | `<INTERN_REVERSE_PROXY_NVT>` |

## Verplichte inhoud

- logisch architectuurdiagram en trustgrenzen;
- VM's, interfaces, adressen en DNS-namen;
- alle inkomende en uitgaande flows;
- beheer-, monitoring- en back-uppaden;
- dataclassificatie en opslaglocaties;
- firewallregels met eigenaar en reden;
- positieve en negatieve testcases;
- benodigde changes aan gedeelde infrastructuur.

## Ontwerpregel

“Het staat op hetzelfde netwerk” is geen securitymodel. Wanneer netwerksegmentatie niet beschikbaar is, documenteer dan welke compensaties gelden: hostfirewall, luisteren op specifieke interfaces, mTLS/TLS, applicatie-authenticatie, aparte serviceaccounts en logging.
