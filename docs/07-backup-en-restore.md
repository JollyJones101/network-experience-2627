# Bestaande backups en herstel

De automatische backupvoorziening is al operationeel. Studenten hoeven geen nieuw backupplatform of eigen parallelle backupstack te bouwen. Eigen projectdata kan volgens de bestaande procedure in de backupvoorziening worden opgenomen.

## Verwachtingen

Documenteer:

- welke eigen data en configuratie beschermd moeten worden;
- welke bestaande job, retentie en opslag daarvoor gebruikt worden;
- verantwoordelijke;
- restoreprocedure;
- testresultaten;
- mislukte tests en verbeteringen.

## Geen installatieopdracht

Het opnieuw opzetten van automatische jobs, backupservers of opslag levert geen punten op. Wijzigingen aan de centrale backupvoorziening verlopen via de docent of de afgesproken changeprocedure.

## Mogelijke herstelscope

Denk afhankelijk van het gekozen project aan:

- data van de onboarded service;
- applicatiedata en configuratie;
- belangrijke VM's/containers;
- OPNsense-configuratie-export zonder secrets waar mogelijk;
- documentatie in Git.

## Hersteltest

Gebruik [templates/backup-test-template.md](templates/backup-test-template.md).

Een hersteltest kan worden vastgelegd met:

- startstatus;
- uitgevoerde stappen;
- resultaat;
- screenshots/logs zonder secrets;
- lessons learned.
