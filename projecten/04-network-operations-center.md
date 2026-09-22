# Project 4 — Network Operations Center

## Opdracht

Bouw een lichtgewicht Network Operations Center voor de studentenprojecten op Smith. Het platform maakt gezondheid, capaciteit en incidenten zichtbaar zonder dat de groep beheerrechten op andere projecten krijgt. De nadruk ligt op betrouwbare signalen, duidelijke eigenaars en bruikbare runbooks — niet op zoveel mogelijk grafieken.

## Must

- Intake bij minstens drie projectgroepen: welke service, eigenaar, SLI en onderhoudsvenster?
- Servicecatalogus met status, afhankelijkheden en contactrol.
- Monitoring van bereikbaarheid, latency, certificaten en overeengekomen applicatiechecks.
- Host- of agentmetrics alleen met toestemming en least-privilege credentials.
- Dashboards voor servicegezondheid, Smith-resourcequota en trends.
- Vier bruikbare alerts: volledige uitval, degradatie, capaciteit en back-up/check-falen.
- Ernstniveaus, deduplicatie, stil onderhoudsvenster en escalatiepad.
- Centrale of gefedereerde logproef voor minstens twee services, met retentie en toegangscontrole.
- Statuspagina die geen interne details of gevoelige metadata lekt.
- Minstens twee gesimuleerde incidenten van detectie tot post-mortem.
- Back-up en restore van configuratie, dashboards en servicecatalogus.

## Should

- SLI/SLO per kritieke dienst en maandrapport met error budget.
- Automatische discovery uit een goedgekeurde bron.
- Synthetic transaction die een echte gebruikersflow test.
- Capacity forecast op basis van gemeten groei.

## Could

- Integratie met n8n voor ticketcreatie en verrijking.
- On-call dashboard en overdrachtsrapport.
- Geanonimiseerde wallboardweergave voor het labo.

## Niet in scope

- cluster- of Proxmox-adminrechten voor monitoring;
- credentials of volledige logs van andere groepen verzamelen;
- onbeperkte high-cardinality metrics;
- alerts zonder eigenaar of actie;
- een zware SIEM installeren zonder resourcebewijs.

## Acceptatietests

| Scenario | Geslaagd wanneer |
|---|---|
| Service down | detectie en melding gebeuren binnen afgesproken tijd, zonder meldingsstorm |
| Trage dienst | synthetic check onderscheidt traag van volledig onbereikbaar |
| Onderhoud | gepland onderhoud onderdrukt alleen de bedoelde alerts en blijft traceerbaar |
| Volle disk | waarschuwing komt vóór uitval en verwijst naar correct runbook |
| Toegangsgrens | operator ziet dashboards maar kan geen broncredentials of andere VM's beheren |
| Restore | dashboards, regels en catalogus worden op een testinstantie hersteld |

## Mijlpalen en bewijs

- Week 2: service-intake en meetbare succescriteria.
- Week 4: toolkeuze en resourcebenchmark.
- Week 6: eerste drie diensten met dashboards.
- Week 8: alerts, logs en runbooks.
- Week 10: incident game day met twee groepen.
- Week 12: SLO-rapport en overdracht.

Lever servicecatalogus, metric- en logarchitectuur, alertmatrix, privacy/retentieanalyse, incidenttijdlijnen, post-mortems en restorebewijs op.
