# Project 7 — Selfservice IT-portaal

## Opdracht

Bouw een veilig selfserviceportaal waarmee studenten of medewerkers gestandaardiseerde IT-aanvragen kunnen indienen en opvolgen. Het portaal automatiseert eenvoudige, vooraf goedgekeurde handelingen en stuurt risicovolle acties eerst door een menselijke goedkeuring. Elke stap moet traceerbaar en omkeerbaar zijn.

Het project draait niet om een mooie verzameling knoppen. Het doel is een betrouwbaar aanvraagproces met duidelijke rechten, validatie, quota, auditlogging en foutafhandeling.

## Gebruikers en stakeholders

- aanvragers: studenten, docenten of projectgroepen;
- goedkeurders: docent, service-eigenaar of gedelegeerde beheerder;
- uitvoerders: beperkte automation-accounts;
- platformbeheerders: de projectgroep en latere opvolgers.

Onderzoek bij minstens drie potentiële gebruikers welke aanvragen vaak terugkomen, hoeveel tijd ze kosten en welke fouten vandaag optreden.

## Must

- Een webportaal met authenticatie en minstens de rollen aanvrager, goedkeurder en platformbeheerder.
- Een dienstencatalogus met minstens vier verschillende aanvraagtypes.
- Minstens twee aanvragen die na geldige goedkeuring veilig geautomatiseerd worden.
- Minstens één aanvraag die bewust alleen een taak of ticket voor een menselijke beheerder oplevert.
- Duidelijke aanvraagstatussen: concept, ingediend, wacht op goedkeuring, in uitvoering, geslaagd, mislukt, ingetrokken en verlopen.
- Server-side validatie, quota en controle op dubbele aanvragen.
- Expliciete menselijke goedkeuring voor acties met impact.
- Een automation-account met alleen de minimaal noodzakelijke rechten.
- Volledige audittrail van aanvrager, goedkeurder, invoer, uitvoering en resultaat, zonder secrets te loggen.
- Foutafhandeling met veilige retry, compensatie of handmatige herstelactie.
- Monitoring van portaal, wachtrij, foutpercentage, doorlooptijd en vastgelopen aanvragen.
- Back-up en restore van configuratie, catalogus, aanvragen en auditgegevens.
- Procedures voor een dienst toevoegen, rechten aanpassen, een aanvraag stoppen en credentials roteren.

## Mogelijke diensten

- aanvraag van een Minecraft-whitelist;
- tijdelijke gameserver aanvragen;
- DNS- of reverse-proxyaanvraag voorbereiden;
- toegang tot een projectdienst aanvragen of intrekken;
- reservatie van een test-VM of afgesproken resource;
- nieuwe repository of projectruimte aanvragen;
- rapport of configuratie-export laten genereren.

De groep kiest diensten die veilig getest kunnen worden. Wijzigingen aan Smith, gedeelde netwerkdiensten of echte organisatieaccounts blijven onder menselijke controle en volgen het changeproces.

## Should

- Geldigheidsduur en automatische intrekking voor tijdelijke toegang.
- Notificaties bij statuswijziging via een goedgekeurd kanaal.
- Service-eigenaar, verwachte levertijd en voorwaarden per catalogusitem.
- Dashboard met aantallen, foutpercentage en mediane doorlooptijd.
- Sandbox of mockprovider voor integratietests.

## Could

- Integratie met n8n als workflowmotor.
- SSO wanneer de opleiding een geschikte koppeling aanbiedt.
- Goedkeuringsregels op basis van rol, quota of risiconiveau.
- API waarmee andere goedgekeurde projecten aanvragen kunnen indienen.

## Niet in scope

- algemene Proxmox-adminrechten aan het portaal geven;
- willekeurige shellcommando's door gebruikers laten invoeren;
- automatische goedkeuring van publieke firewall- of netwerkchanges;
- credentials in formulieren, broncode of auditlogs opslaan;
- echte accounts of resources verwijderen zonder geteste compensatie en expliciete toestemming.

## Acceptatietests

| Scenario | Geslaagd wanneer |
|---|---|
| Geldige aanvraag | juiste goedkeurder ontvangt de aanvraag en uitvoering levert precies één resultaat |
| Afkeuring | er wordt niets uitgevoerd en de reden is zichtbaar voor de aanvrager |
| Dubbele aanvraag | dezelfde idempotente aanvraag maakt geen dubbele resource of toegang |
| Onbevoegde gebruiker | kan geen aanvraag goedkeuren, catalogus wijzigen of automation-secret bekijken |
| Ongeldige invoer | wordt vóór uitvoering geweigerd met bruikbare foutmelding |
| Providerstoring | aanvraag blijft traceerbaar, retries zijn begrensd en beheerder krijgt een alert |
| Intrekking | tijdelijke toegang of resource wordt volgens afspraak veilig verwijderd |
| Restore | catalogus, open aanvragen en audittrail worden in een testomgeving hersteld |

## Mijlpalen

- Week 2: procesinventaris, gebruikersinterviews en selectie van vier diensten.
- Week 4: rollen-, dataflow- en integratieontwerp plus mockproof.
- Week 6: portaal en één end-to-end aanvraag.
- Week 8: volledige catalogus, audit, monitoring en back-up.
- Week 10: pilot met representatieve gebruikers en gemeten tijdswinst.
- Week 12: stabiele release, beheerrunbooks en overdracht.

## Verplichte bewijsstukken

Procesanalyse voor en na, dienstencatalogus, architectuur- en dataflowdiagram, rollenmatrix, automation-permissions, state-diagram van een aanvraag, auditvoorbeelden, foutscenario's, gebruikerstest, restorebewijs en beheerdershandleiding.
