# Services ontwerpen en beheren

De gekozen technologie is een middel, geen projectdoel. Kies de kleinste begrijpelijke architectuur die de Must-eisen betrouwbaar haalt binnen het Smith-budget.

## Selectiecriteria

Vergelijk voor kritieke componenten:

- actieve ondersteuning en securityhistoriek;
- licentie en toegestaan gebruik;
- resourceverbruik bij normale en piekbelasting;
- integratiemogelijkheden;
- authenticatie en rollen;
- back-up- en exportmogelijkheden;
- upgradepad en rollback;
- beheercomplexiteit voor de volgende groep.

Leg de beslissing kort vast als Architecture Decision Record of in het projectcharter.

## Per service

Gebruik [service-template.md](templates/service-template.md) en documenteer:

- doel, eigenaar en gebruikers;
- versie, bron en updatebeleid;
- host, resources en netwerkflows;
- configuratie en deployment zonder secrets;
- accounts, rollen en dataclassificatie;
- monitoring, logs en alerts;
- back-up, restore en rollback;
- bekende beperkingen en stopprocedure.

## Vermijd

- Kubernetes of een zware enterprise-stack alleen voor de technologie;
- meer componenten dan de groep kan patchen en herstellen;
- dashboards zonder actie;
- databases of beheerinterfaces die op alle interfaces luisteren;
- images met onduidelijke herkomst of een floating latest-tag;
- één handmatig ingerichte VM waarvan niemand de exacte opbouw kan reproduceren.
