# Change management

Een change request is nodig zodra een wijziging merkbare productie-impact kan hebben of een grens van de eigen groep overschrijdt.

## Altijd vooraf aanvragen

- DNS, certificaten, reverse proxy of publieke bereikbaarheid;
- VLAN, bridge, routing, firewall of gedeelde netwerkdienst;
- extra resources boven het goedgekeurde budget;
- aansluiting van switches, access points, DHCP, caching of eventinfrastructuur;
- integratie met echte accounts, mailinglijsten of organisatie-API's;
- belastende load-, security- of failovertest;
- verwerking van persoonsgegevens;
- downtime of een destructieve actie op een gebruikte dienst.

## Inhoud

Gebruik [change-request-template.md](docs/templates/change-request-template.md) en beschrijf doel, scope, impact, risico, onderhoudsvenster, communicatie, stappen, eigenaar, validatie en rollback.

## Beslissing

Een change heeft één van deze statussen:

- **draft:** nog niet klaar voor beoordeling;
- **requested:** volledig en wacht op beslissing;
- **approved:** mag binnen het afgesproken venster worden uitgevoerd;
- **rejected:** wordt niet uitgevoerd; reden is vastgelegd;
- **implemented:** uitgevoerd en gevalideerd;
- **rolled back:** teruggedraaid en geëvalueerd.

Stilte is geen goedkeuring. Een mondeling akkoord wordt door de groep kort schriftelijk bevestigd.

## Na uitvoering

Noteer werkelijke start/eindtijd, afwijkingen, metingen, testresultaten, incidenten en bijgewerkte documentatie. Sluit pas wanneer de service stabiel is en eventuele tijdelijke toegang is ingetrokken.
