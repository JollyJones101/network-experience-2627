# Project 6 — Cyber Range & CTF

## Opdracht

Bouw een volledig geïsoleerde cyber range en organiseer een educatieve capture-the-flag voor medestudenten. De groep combineert netwerksegmentatie, challengebeheer, scoring, observability, resetbaarheid en didactiek. Veiligheid is de eerste acceptatievoorwaarde.

## Must

- Schriftelijk goedgekeurde scope, doelgroep en spelregels.
- Gescheiden deelnemers-, challenge- en beheerzone binnen de toegewezen netwerkmogelijkheden.
- Geen route naar Smith-beheer, andere groepen of campusdiensten vanuit challenges.
- CTF-platform met teams, scorebord, start/eindtijd en gecontroleerde registratie.
- Minstens zes zelfgemaakte of aantoonbaar gelicentieerde challenges, verdeeld over drie categorieën en twee moeilijkheidsniveaus.
- Elke challenge heeft leerdoel, hintstrategie, unieke flag, oplossing en resetprocedure.
- Reproduceerbare deployment en snelle reset van de challengeomgeving.
- Rate limiting, resourcegrenzen en logging zonder onnodige opslag van deelnemersverkeer.
- Monitoring van beschikbaarheid, errors en resource-uitputting.
- Dry-run met testteam, formele escape-test en incident/kill-switchprocedure.

## Should

- Dynamische flags of afzonderlijke instanties waar haalbaar.
- Feedbackformulier dat leerdoelen meet.
- Automatisch openen/sluiten en resetten van challenges.
- Blue-teamdashboard met alleen noodzakelijke events.

## Could

- Verhaallijn en visuele branding.
- Samenwerking met n8n voor goedgekeurde notificaties.
- Jeopardyfinale of bonuschallenge zonder extra risico.

## Niet in scope

- aanvallen op publieke doelen, campusnetwerk, Smith-host of andere groepen;
- malware, persistence of command-and-control buiten de afgesloten range;
- echte credentials of persoonsgegevens in challenges;
- challenges die internettoegang nodig hebben tijdens exploitatie;
- tools of instructies gebruiken buiten het afgesproken evenement.

## Acceptatietests

| Scenario | Geslaagd wanneer |
|---|---|
| Segmentatie | challenge kan toegelaten doelen bereiken maar geen campus-, Smith- of andere groepsresources |
| Unieke flags | flag van challenge/team A werkt niet onbedoeld voor een ander doel |
| Reset | corrupte challenge wordt binnen afgesproken tijd schoon teruggezet |
| Misbruik | rate/resourcegrens beperkt een gecontroleerde overbelasting |
| Score | correcte inzending scoort eenmaal; fout of dubbel event wordt correct afgehandeld |
| Kill switch | verantwoordelijke kan de range gecontroleerd isoleren |
| Leerdoel | testdeelnemers begrijpen na afloop de bedoelde kwetsbaarheid en mitigatie |

## Mijlpalen en bewijs

- Week 2: regels, leerdoelen en risicokader.
- Week 4: isolatieontwerp en één veilige voorbeeldchallenge.
- Week 6: platform en zes challengeprototypes.
- Week 8: reset, monitoring, escape-tests en runbooks.
- Week 10: gesloten dry-run en fixes.
- Week 12: goedgekeurde CTF of volledige simulatie, write-ups en cleanup.

Lever netwerk- en trustboundarydiagram, threat model, challengecatalogus, deploymentcode, escape-testbewijs, draaiboek, geanonimiseerd incidentlog, feedbackanalyse en cleanupbewijs op.
