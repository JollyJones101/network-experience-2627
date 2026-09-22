# Project 1 — Minecraft Community Platform

## Opdracht

Bouw een snelle, stabiele en eenvoudig te beheren Minecraft-dienst voor de opleiding. Het platform is geen losse gameserver: het krijgt een duidelijke communitystructuur, veilige rollen, moderatie, monitoring, back-up, updatebeleid en overdracht. Studenten en personeelsleden moeten zonder technische voorkennis kunnen deelnemen; beheerders moeten incidenten en upgrades gecontroleerd kunnen afhandelen.

## Opdrachtgever en gebruikers

- opdrachtgever: opleiding of aangeduide docent;
- spelers: studenten van meerdere jaren en eventueel personeel;
- staff: helpers, moderators en beheerders;
- technisch beheer: huidige groep, later overdraagbaar aan opvolgers.

Interview vóór het ontwerp minstens één docent, twee spelers en één mogelijke moderator. Leg afspraken vast over spelmodus, toegangsbeleid, gedragscode, bewaartermijn en eigenaarschap na het vak.

## Must

- Een geoptimaliseerde Java-server met gemotiveerde keuze voor bijvoorbeeld Paper, Purpur of een vergelijkbare ondersteunde variant.
- Een afgeschermde acceptatieomgeving of testkopie zodat updates niet rechtstreeks op productie worden uitgeprobeerd.
- Whitelist of gekoppeld registratieproces; geen anonieme adminrechten.
- Rollenmodel met minstens speler, helper, moderator en administrator.
- Least-privilege permissions; operatorrechten alleen waar strikt nodig.
- Een lobby/spawn, gedragscode, onboarding en duidelijke contactroute voor meldingen.
- Moderatietools voor waarschuwing, mute, kick, tijdelijke/permanente ban en auditlog.
- Bescherming tegen griefing met rollbackmogelijkheid en aantoonbare hersteltest.
- Veilige remote console of beheerinterface die niet publiek openstaat.
- Automatische world- en configuratieback-up met retentie en een geteste restore naar een aparte testwereld.
- Monitoring van bereikbaarheid, tick rate/TPS, CPU, RAM, disk, spelersaantal en back-upstatus.
- Een onderbouwde capaciteitstest met meerdere testclients of gecontroleerde loadsimulatie.
- Update-, plugin-, incident-, moderatie- en restore-runbooks.

## Should

- BlueMap of een vergelijkbare kaart, met afzonderlijke publicatie- en privacyafweging.
- Geplande restart met waarschuwingen, save en gecontroleerde herstart.
- Automatische melding bij downtime, lage TPS, bijna volle disk of mislukte back-up.
- Selfservice-aanvraag voor whitelist, met expliciete goedkeuring en audittrail.
- Seizoens- of eventkalender en proces om tijdelijk extra moderators aan te stellen.
- Stagingtest die pluginversies en configuratie vóór productie valideert.

## Could

- Een proxy en tweede spelmodus, alleen als de single-serverbasis stabiel en meetbaar binnen budget is.
- Bedrock-toegang via een compatibiliteitslaag, na security- en supportanalyse.
- Integratie met het n8n-project voor aanvragen en meldingen.
- Geanonimiseerd publieksdashboard met uptime en spelersaantal.

## Niet in scope

- pay-to-win, verkoop of kansspelen;
- cracked/offline authenticatie;
- plugins of maps zonder controle op licentie en herkomst;
- onbeperkte pregeneration of loadtests op Smith;
- een publiek onbeheerd RCON- of beheerpaneel;
- persoonlijke spelersdata langer bewaren dan nodig.

## Technische ontwerpvragen

- Welke software en Java-versie bieden de beste balans tussen compatibiliteit en performance?
- Welke view-distance, simulation-distance, garbage collector en pregeneration passen binnen het quota?
- Welke data moet crash-consistent worden opgeslagen?
- Hoe voorkom je dat een plugin alle rechten of resources krijgt?
- Hoe worden logs bruikbaar gehouden zonder chat onnodig lang te bewaren?
- Hoe herstel je één beschadigde regio, één spelersactie en de volledige wereld?

## Acceptatietests

| Test | Geslaagd wanneer |
|---|---|
| Speler onboarding | een nieuwe toegelaten speler kan verbinden en ziet regels; een onbekende gebruiker wordt geweigerd |
| Rollen | helper en moderator kunnen alleen afgesproken acties; geen van beide krijgt server- of OS-admin |
| Moderatie | waarschuwing/ban is zichtbaar in auditlog en kan gecontroleerd worden teruggedraaid |
| Performance | afgesproken testbelasting blijft binnen vastgelegde TPS-, RAM- en CPU-grenzen |
| Griefherstel | een gecontroleerde wijziging wordt binnen de afgesproken tijd hersteld |
| Back-up | een wereld en configuratie worden naar een aparte testlocatie hersteld en gestart |
| Failure | onverwachte serverstop veroorzaakt geen onverklaard dataverlies; alert bereikt de juiste eigenaar |
| Security | beheerpoorten zijn vanaf een niet-toegelaten netwerk onbereikbaar |

## Mijlpalen

- Week 2: communitycharter, doelgroep, spelregels en succesmetingen.
- Week 4: softwarebenchmark, architectuur en pluginrisicoanalyse.
- Week 6: speelbare interne alpha met rollen en logging.
- Week 8: monitoring, back-up, herstel en moderatieproces.
- Week 10: beperkte communitytest en feedback.
- Week 12: stabiele release, beheeroverdracht en toekomstbesluit.

## Verplichte bewijsstukken

Architectuur- en netwerkdiagram, pluginregister met doel/bron/versie, permissionsmatrix, resourcebenchmark, moderatieprocedure, geanonimiseerde auditlog, back-up- en herstelbewijs, testverslag met spelersfeedback en een korte gebruikersgids.
