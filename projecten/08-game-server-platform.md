# Project 8 — Game Server as a Service

## Opdracht

Bouw een beheerd platform waarop een bevoegde gebruiker tijdelijk een goedgekeurde gameserver kan aanvragen, starten, stoppen en laten opruimen. Het platform ondersteunt meerdere serverprofielen, maar bewaakt strikt de beschikbare resources op Smith.

Dit is breder dan één Minecraft-server: de kern is lifecyclebeheer, isolatie, quota, veilige templates, monitoring en automatische cleanup van tijdelijke gameomgevingen.

## Gebruikers en stakeholders

- spelers of organisatoren die tijdelijk een server nodig hebben;
- docent of moderator die aanvragen en toegelaten games beheert;
- platformoperators die templates, capaciteit en incidenten opvolgen;
- Smith-beheerder die de maximale infrastructuurgrens bepaalt.

## Must

- Een catalogus van minstens drie technisch verschillende, legaal bruikbare gameprofielen.
- Per profiel: ondersteunde versie, poorten, minimum/maximum resources, persistentie, licentievoorwaarden en updateprocedure.
- Aanvraagproces met eigenaar, doel, gewenste looptijd, spelerslimiet en goedkeuring.
- Geautomatiseerde deployment vanuit versievaste templates of configuratiecode.
- Unieke serveridentiteit en gescheiden data/configuratie per aanvraag.
- Groepsbreed quota voor gelijktijdige servers, vCPU, RAM, disk en maximale levensduur.
- Veilige publicatie: alleen noodzakelijke spelpoorten; beheerpaneel en console niet publiek.
- Rollen voor aanvrager, serveroperator, moderator en platformbeheerder.
- Start, stop, geplande restart, verlenging en gecontroleerde verwijdering.
- Automatische waarschuwing vóór verval en cleanup na het bewaarbeleid.
- Monitoring van bereikbaarheid, spelersaantal waar beschikbaar, CPU, RAM, disk en crashloops.
- Back-upoptie voor gemarkeerde persistente servers en aantoonbare restore.
- Auditlog van aanvraag, goedkeuring, lifecycleacties en templateversie.

## Should

- Test/staging van nieuwe servertemplates vóór opname in de catalogus.
- Mods of plugins via een goedgekeurde allowlist en versiecontrole.
- Statuspagina met serverstatus zonder beheerinformatie te lekken.
- Automatische geplande schaal- of stopactie bij langdurige inactiviteit.
- Kosten- of resource-unit per aangevraagde server zichtbaar maken.

## Could

- Selfserviceportaal uit project 7 als front-end.
- Integratie met de LAN-party voor vooraf goedgekeurde eventservers.
- Savegame-export bij beëindiging met beperkte downloadtijd.
- Wachtlijst wanneer het resourcebudget volzet is.

## Niet in scope

- willekeurige images, mods of binaries door gebruikers laten uitvoeren;
- privileged containers, Smith-hostmounts of brede Docker-sockettoegang;
- cracked authenticatie of illegaal verkregen gamebestanden;
- onbeperkte serverduur of resources;
- automatische publieke port forwards buiten het goedgekeurde netwerkpad;
- commerciële verhuur of verwerking van betalingen.

## Acceptatietests

| Scenario | Geslaagd wanneer |
|---|---|
| Nieuwe server | goedgekeurde aanvraag levert reproduceerbaar een bereikbare server uit het gekozen profiel |
| Quota | aanvraag boven groeps- of profielgrens wordt veilig geweigerd of op wacht gezet |
| Isolatie | operator van server A kan data, console of secrets van server B niet benaderen |
| Templatefout | mislukte deployment laat geen half beheerde resources of open poorten achter |
| Inactiviteit/verval | waarschuwing en automatische stop/cleanup volgen het afgesproken beleid |
| Update | nieuwe template wordt eerst getest en bestaande server kan gecontroleerd terugrollen |
| Crash | monitoring detecteert de fout zonder oneindige restartloop |
| Restore | save/configuratie van een persistente testserver wordt in een nieuwe instantie hersteld |

## Mijlpalen

- Week 2: gebruikersflows, gamecatalogus en licentie-/resourceonderzoek.
- Week 4: template-, netwerk-, quota- en lifecycleontwerp.
- Week 6: eerste twee profielen volledig automatisch inzetbaar.
- Week 8: derde profiel, rollen, monitoring, expiry en back-up.
- Week 10: pilot met meerdere gelijktijdige servers en gebruikers.
- Week 12: gevalideerde catalogus, capaciteitsrapport en overdracht.

## Verplichte bewijsstukken

Gameprofielcatalogus, licentie- en herkomstregister, architectuur, netwerkflows, templatecode, quotamodel, capaciteitstest, rollenmatrix, cleanupbewijs, update/rollbacktest, restoretest en operatorhandleiding.
