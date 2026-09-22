# Projectcatalogus

Elke groep realiseert één project als een kleine productieopdracht. De docent bepaalt samen met de groep de definitieve scope, het testpubliek en de resourcegrens. De projecten zijn verschillend van onderwerp, maar gelijkwaardig in technische en organisatorische diepgang.

## Keuzematrix

| # | Project | Zwaartepunt | Richtgrootte | Belangrijkste afhankelijkheid |
|---:|---|---|---:|---|
| 1 | [Minecraft Community Platform](01-minecraft-community.md) | performance, rollen, moderatie, back-up | 3–4 | testspelers en publicatiepad |
| 2 | [n8n Automation Hub](02-n8n-automation-hub.md) | workflows, API's, betrouwbaarheid, secrets | 3–4 | bruikbare processen en API-toegang |
| 3 | [LAN-party van A tot Z](03-lan-party.md) | event, netwerk, caching, communicatie | 4–5 | toestemming Stuvo, lokaal en IT |
| 4 | [Network Operations Center](04-network-operations-center.md) | metrics, logs, alerts, incidenten | 3–4 | medewerking van andere projectgroepen |
| 5 | [Forge & Ship](05-forge-ci-platform.md) | Git, CI/CD, registry, runners | 3–4 | veilige runnerisolatie |
| 6 | [Cyber Range & CTF](06-cyber-range-ctf.md) | isolatie, challenges, scoring, veiligheid | 4–5 | goedgekeurde netwerkisolatie |
| 7 | [Selfservice IT-portaal](07-selfservice-it-portaal.md) | aanvragen, approvals, automation, audit | 3–4 | veilige API's of mocks |
| 8 | [Game Server as a Service](08-game-server-platform.md) | templates, lifecycle, quota, isolatie | 3–4 | toegelaten games en publicatiepad |
| 9 | [Studentencloud](09-studentencloud.md) | filesharing, quota, privacy, restore | 3–4 | voldoende storage en databeleid |
| 10 | [Digitale servicedesk](10-digitale-servicedesk.md) | supportprocessen, SLA's, kennisbank | 3–4 | representatieve gebruikers en oefening |

## Gemeenschappelijke minimumeisen

Elke projectgroep moet:

1. het probleem valideren bij minstens één opdrachtgever en drie representatieve gebruikers;
2. een expliciete Must / Should / Could / Won't-scope vastleggen;
3. alle VM's binnen de toegewezen Smith-pool en het resourcebudget houden;
4. deployment en minstens één terugkerende beheerhandeling automatiseren;
5. authenticatie, rollen, netwerkregels, updates en secrets aantoonbaar beheren;
6. dashboards en bruikbare alerts met eigenaar en reactieprocedure voorzien;
7. niet-reproduceerbare data back-uppen en een restore uitvoeren;
8. een normale gebruikersflow én een fout- of aanvalsscenario testen;
9. gebruikers-, beheer- en overdrachtsdocumentatie opleveren;
10. na de test tijdelijke accounts, data en ongebruikte VM's gecontroleerd opruimen.

## Scope bewaken

De Must-sectie van de gekozen fiche is de kernopdracht. Should wordt pas opgenomen als de kern stabiel is. Could levert alleen meerwaarde op als de groep de impact kan beheren. Een technisch opvallende uitbreiding weegt niet op tegen ontbrekende monitoring, security of documentatie.

## Eigen voorstel

Een eigen voorstel kan wanneer het minstens dezelfde breedte heeft: een echte doelgroep, meerdere technische componenten, netwerk- en securitykeuzes, automatisering, operations en een realistische acceptatietest. Gebruik de structuur van de bestaande fiches en laat het charter vóór week 3 goedkeuren.
