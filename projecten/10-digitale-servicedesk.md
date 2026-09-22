# Project 10 — Digitale servicedesk

## Opdracht

Bouw een volwaardige servicedesk voor supportvragen, incidenten, service requests en changes binnen de opleiding. Het platform moet gebruikers een eenvoudige ingang geven en beheerders helpen prioriteren, communiceren, meten en kennis hergebruiken.

De waarde zit niet alleen in ticketsoftware installeren. De groep ontwerpt een werkbaar serviceproces, configureert rollen en SLA's, automatiseert repetitieve stappen en test de werking tijdens een realistische supportoefening.

## Gebruikers en stakeholders

- studenten en docenten als melders;
- eerstelijns support;
- tweedelijns technisch beheer;
- service-eigenaars en change-goedkeurders;
- docent of opleidingsverantwoordelijke als opdrachtgever.

Analyseer minstens tien representatieve voorbeeldmeldingen en bepaal welke categorie, prioriteit en route ze nodig hebben.

## Must

- Een toegankelijk webportaal met persoonlijke accounts en e-mail alleen als een veilig test- of goedgekeurd kanaal beschikbaar is.
- Afzonderlijke processen of formulieren voor incident, service request, supportvraag en change.
- Rollen voor melder, supportmedewerker, specialist, change-goedkeurder en platformbeheerder.
- Servicecatalogus en categorieboom die gebruikers begrijpen.
- Prioriteitsmatrix op basis van impact en urgentie; prioriteit mag niet alleen door de melder bepaald worden.
- Ticketworkflow met eigenaar, status, interne notitie, reactie aan gebruiker, escalatie en sluitreden.
- SLA- of streeftijden per prioriteit met pauzevoorwaarden en zichtbare overschrijding.
- Automatische routering of taaktoewijzing voor minstens drie categorieën.
- Kennisbank met minstens acht bruikbare artikels gebaseerd op echte of gesimuleerde veelgestelde vragen.
- Tevredenheidsvraag en heropeningsprocedure.
- Dashboards voor volume, backlog, leeftijd, eerste reactietijd, oplostijd, SLA en heropeningen.
- Monitoring, back-up/restore en procedures voor update, accountbeheer en storing.
- Een realistische supportoefening met minstens vijftien tickets en meerdere behandelaars.

## Should

- Detectie of koppeling van dubbele meldingen rond één storing.
- Problem record voor terugkerende incidenten met oorzaak en structurele actie.
- Goedgekeurde e-mailsjablonen en automatische ontvangstbevestiging.
- CMDB-light met alleen relevante services, eigenaar en afhankelijkheden.
- Privacyvriendelijke export voor maandrapportage.

## Could

- Integratie met n8n voor veilige ticketverrijking of notificatie.
- Monitoringalert die na deduplicatie één incident opent.
- Selfservice-acties vanuit goedgekeurde kennisartikels.
- Feedback van andere projectgroepen als tijdelijke servicedeskklanten.

## Niet in scope

- echte mailboxen of mailinglijsten zonder toestemming gebruiken;
- wachtwoorden, tokens of gevoelige logs in tickets opslaan;
- supportmedewerkers standaard platformadmin maken;
- misleidende SLA-beloftes zonder bezetting of escalatie;
- gebruikersactiviteit inzetten als individuele prestatiemonitoring;
- automatisch tickets sluiten zonder controle of communicatie.

## Acceptatietests

| Scenario | Geslaagd wanneer |
|---|---|
| Nieuw incident | juiste categorie, prioriteit en supportgroep worden bepaald en ontvangst is zichtbaar |
| Urgente storing | impact/urgentie leiden tot correcte escalatie en timing |
| Gewone aanvraag | volgt een andere workflow dan een incident en vereist waar nodig goedkeuring |
| Onbevoegde toegang | melder ziet geen privénotities of tickets van anderen; agent krijgt geen platformadmin |
| SLA | timer start, pauzeert en stopt volgens de gedocumenteerde voorwaarden |
| Duplicaten | meerdere meldingen rond één storing blijven gezamenlijk communiceerbaar |
| Kennisartikel | representatieve gebruiker lost een gekozen probleem zonder hulp op |
| Restore | tickets, bijlagen, kennisbank en rechten worden in een testomgeving hersteld |

## Supportoefening

Laat een docent of andere groep een scenario aanbieden met minstens:

- één brede storing met meerdere meldingen;
- één securitygevoelige melding;
- één onduidelijke aanvraag die triage vraagt;
- één change met goedkeuring;
- één terugkerend probleem;
- één ontevreden gebruiker of heropend ticket.

Meet de doorlooptijd, kwaliteit van communicatie, correcte escalatie en bruikbaarheid van de kennisbank. Gebruik geen echte secrets of persoonsgegevens in de oefening.

## Mijlpalen

- Week 2: serviceblauwdruk, ticketanalyse en prioriteitsmatrix.
- Week 4: platformkeuze, workflows, rollen en databeleid.
- Week 6: incident- en requestproces bruikbaar.
- Week 8: change, kennisbank, SLA's, dashboards en back-up.
- Week 10: supportoefening en gebruikerstest.
- Week 12: verbeterde processen, maandrapport en overdracht.

## Verplichte bewijsstukken

Serviceblauwdruk, categorie- en prioriteitsmodel, workflowdiagrammen, rollenmatrix, SLA-definities, kennisbank, automationregels, geschoonde oefendataset, dashboardanalyse, restorebewijs, supporthandboek en verbeterplan na de oefening.
