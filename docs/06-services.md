# Services

Elke service moet bewust gekozen, licht genoeg en professioneel gedocumenteerd zijn.

## Projectkeuze

De lijst met mogelijke studentenprojecten staat uitsluitend in [backlog.md](../backlog.md). Dit document bevat alleen algemene aandachtspunten voor services.

De reverse proxy, VPN, SSO, NetBox en automatische backupvoorziening zijn al aanwezig en zijn afhankelijkheden, geen extra services die groepen opnieuw installeren.

## Vermijd zware keuzes

- volledige Kubernetes-clusters;
- zware Nextcloud-installaties zonder resourcebewijs;
- meerdere Windows Servers;
- grote databases;
- uitgebreide SIEM-stacks;
- te veel services tegelijk.

## Algemene documentatie per service

Gebruik [templates/service-template.md](templates/service-template.md). Beschrijf minstens:

- doel;
- eigenaar;
- installatie;
- configuratie;
- netwerkpad;
- firewallregels;
- authenticatie;
- back-up;
- monitoring;
- testprocedure;
- rollback.
