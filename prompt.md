Je bent een technische onderwijsassistent en repository-architect. Bouw deze repository volledig van nul op voor het OPO **Network Experience**.

## Context van het vak

Network Experience is het laatste netwerk- en systeembeheervak voor studenten **Elektronica-ICT, afstudeerrichting ICT, 3de jaar**. Het vak moet aanvoelen als een realistische eindopdracht waarin studenten een kleine bedrijfsomgeving beheren.

Er zullen ongeveer **30 studenten** zijn. Studenten werken in groepen van ongeveer **3 studenten**. Elke groep krijgt een eigen virtuele labo-omgeving.

De nieuwe labo-opzet is als volgt:

```text
Fysieke Proxmoxcluster van de opleiding
└── Per studentengroep: één "doos-Proxmox" VM
    ├── OPNsense VM
    │   ├── WAN: verbinding naar buiten/opleidingsnetwerk
    │   └── LAN: intern groepsnetwerk
    ├── Proxmox node 1 VM
    ├── Proxmox node 2 VM
    └── Proxmox node 3 VM
```

Belangrijk didactisch uitgangspunt:

* De docent beheert de fysieke Proxmoxcluster en de bovenliggende **doos-Proxmox**.
* Studenten krijgen **geen beheerrechten op de doos-Proxmox**.
* Studenten krijgen wel beheerrechten op:

  * hun OPNsense VM;
  * hun drie virtuele Proxmox-nodes;
  * de VM’s en containers die ze zelf binnen hun Proxmox-cluster aanmaken.
* De virtuele bekabeling is vooraf correct opgezet door de docent, zodat alle Proxmox-nodes achter OPNsense zitten.
* Studenten mogen OPNsense, firewallregels, VPN, Proxmox-cluster, services, monitoring, logging en back-ups zelf configureren.
* Studenten mogen de onderliggende virtuele infrastructuur niet bypassen door nodes rechtstreeks op het WAN te hangen.

De vorige repo van het vak bevatte onder andere:

* `README.md` met vakbeschrijving, leerdoelen, planning en evaluatie;
* `Afspraken.md` met praktische afspraken;
* `Spelregels.md` met randvoorwaarden rond veiligheid, hardware, netwerk, accounts en change management;
* `Github.md` met werkwijze rond Issues, Pull Requests, changelog en documentatie;
* `IterationPlan.md` met backlog per iteration;
* `Evaluation.md` met evaluatierubric;
* `SupportTickets.md`;
* een hardware-inventaris-template;
* OPNsense-installatiemateriaal;
* een GitHub issue template;
* een GitHub Action die bij gesloten issues automatisch een changelog aanvult.

Gebruik deze stijl als inspiratie, maar bouw de repo opnieuw op rond de nieuwe virtuele groepsomgeving.

## Doel van de repo

De repository moet bruikbaar zijn als centrale cursus- en projectrepo voor studenten. Ze moet uitleg geven over:

1. Wat het vak inhoudt.
2. Hoe de labo-omgeving werkt.
3. Wat studenten wel en niet mogen aanpassen.
4. Hoe groepen samenwerken.
5. Hoe GitHub gebruikt wordt.
6. Welke deliverables verwacht worden.
7. Hoe evaluatie gebeurt.
8. Hoe studenten hun infrastructuur moeten documenteren.
9. Hoe supporttickets, incidenten en wijzigingen gelogd worden.
10. Hoe de eindoplevering eruitziet.

Schrijf alles in helder, professioneel Nederlands, gericht aan studenten. De toon mag duidelijk en kordaat zijn, maar niet betuttelend.

## Belangrijke inhoudelijke keuzes

Werk de repo uit vanuit dit model:

* Elke groep beheert een eigen kleine bedrijfsomgeving.
* OPNsense is de edge firewall/router.
* De drie Proxmox-nodes vormen een cluster.
* Binnen dat cluster bouwen studenten zelf services.
* Security, documentatie, change management en troubleshooting zijn even belangrijk als “het werkt”.
* Studenten moeten aantonen dat hun omgeving achter OPNsense zit.
* Studenten moeten kunnen uitleggen waarom ze bepaalde netwerk- en systeembeheerkeuzes maken.
* Fouten maken mag, maar fouten verzwijgen niet.
* Geen wachtwoorden, tokens, private keys of certificaatsleutels in GitHub.
* Geen aanpassingen aan de onderliggende doos-Proxmox zonder toestemming van de docent.
* Geen rechtstreekse toegang van studentennodes naar het WAN buiten OPNsense om.

## Maak deze repositorystructuur

Maak minstens deze structuur aan:

```text
.
├── README.md
├── roadmap.md
├── evaluatie.md
├── praktische-afspraken.md
├── spelregels.md
├── github-werkwijze.md
├── changelog.md
├── backlog.md
├── groepsindeling.md
├── eindoplevering.md
├── supporttickets.md
├── incidenten.md
├── change-management.md
├── docs/
│   ├── 00-start-here.md
│   ├── 01-labo-architectuur.md
│   ├── 02-toegang-en-accounts.md
│   ├── 03-opnsense.md
│   ├── 04-proxmox-cluster.md
│   ├── 05-netwerkplan.md
│   ├── 06-services.md
│   ├── 07-backup-en-restore.md
│   ├── 08-monitoring-en-logging.md
│   ├── 09-security-hardening.md
│   ├── 10-documentatie-template.md
│   ├── templates/
│   │   ├── netwerkplan-template.md
│   │   ├── server-template.md
│   │   ├── service-template.md
│   │   ├── firewall-rule-template.md
│   │   ├── backup-test-template.md
│   │   ├── incident-report-template.md
│   │   └── change-request-template.md
│   └── docent/
│       └── docent-checklist.md
├── configs/
│   └── README.md
├── diagrams/
│   └── README.md
├── images/
│   └── README.md
├── scripts/
│   └── README.md
└── .github/
    ├── ISSUE_TEMPLATE/
    │   ├── project.yml
    │   ├── support.yml
    │   ├── incident.yml
    │   ├── question.yml
    │   └── change-request.yml
    ├── pull_request_template.md
    └── workflows/
        └── issue-changelog.yml
```

Je mag extra bestanden toevoegen als dat zinvol is.

## Inhoud per bestand

### README.md

Maak een sterke startpagina met:

* titel: Network Experience;
* korte introductie;
* voor wie het vak bedoeld is;
* wat studenten gaan bouwen;
* overzicht van de labo-architectuur;
* kernverwachtingen;
* link naar `docs/00-start-here.md`;
* korte uitleg van de evaluatie;
* verwijzing naar spelregels en praktische afspraken.

Maak duidelijk dat dit geen klassiek stappenplanvak is, maar een geïntegreerde eindopdracht waarin studenten zelf keuzes moeten maken, testen en verantwoorden.

### docs/00-start-here.md

Maak een startgids voor studenten met:

* wat ze eerst moeten lezen;
* wat ze tijdens de eerste les moeten controleren;
* welke gegevens ze van de docent krijgen;
* hoe ze hun groepsmap/documentatie opstarten;
* checklist voor week 1.

### docs/01-labo-architectuur.md

Leg de technische architectuur uit met ASCII-schema’s.

Neem zeker dit model op:

```text
Fysieke Proxmoxcluster opleiding
└── Doos-Proxmox groep X
    ├── OPNsense
    │   ├── WAN
    │   └── LAN
    ├── pve-x-01
    ├── pve-x-02
    └── pve-x-03
```

Leg uit:

* wat de fysieke laag is;
* wat de doos-Proxmox is;
* waarom studenten daar geen beheerrechten op krijgen;
* wat OPNsense doet;
* wat de drie Proxmox-nodes doen;
* waarom alle verkeer via OPNsense moet lopen;
* hoe dit lijkt op een kleine bedrijfsomgeving.

Voorzie placeholders voor IP-plannen, bijvoorbeeld:

```text
Groep X LAN: 172.16.X.0/24
OPNsense LAN: 172.16.X.1
Proxmox node 1: 172.16.X.11
Proxmox node 2: 172.16.X.12
Proxmox node 3: 172.16.X.13
```

Zet erbij dat exacte IP-ranges door de docent bevestigd worden.

### docs/02-toegang-en-accounts.md

Documenteer:

* welke accounts studenten krijgen;
* waar ze mogen inloggen;
* waar ze niet mogen inloggen;
* hoe ze omgaan met wachtwoorden;
* waarom secrets nooit in GitHub mogen;
* wat ze doen bij verloren toegang;
* hoe ze adminacties loggen.

### docs/03-opnsense.md

Maak een gids rond OPNsense met:

* rol van OPNsense in de opdracht;
* WAN/LAN-concept;
* basischecks;
* DHCP/DNS;
* firewallregels;
* NAT;
* VPN als mogelijke opdracht;
* bewijs dat de Proxmox-nodes achter OPNsense zitten;
* wat studenten niet mogen doen.

Geen volledige klikhandleiding schrijven, maar wel duidelijke technische verwachtingen en documentatievereisten.

### docs/04-proxmox-cluster.md

Leg uit wat studenten moeten realiseren:

* drie Proxmox-nodes controleren;
* cluster vormen;
* node naming;
* storagekeuzes documenteren;
* VM/CT-netwerken;
* users/roles;
* basis hardening;
* test-VM of test-container aanmaken;
* failoverconcept bespreken indien relevant;
* beperkingen van nested virtualization vermelden.

Leg uit dat dit een labo-omgeving is en geen productiecluster met volledige performance.

### docs/05-netwerkplan.md

Maak een document dat uitlegt wat in een goed netwerkplan moet staan:

* subnetten;
* gateway;
* DNS;
* DHCP-scope;
* VLANs indien gebruikt;
* firewallzones;
* firewallregels;
* beheerinterfaces;
* services;
* diagram;
* testplan.

### docs/06-services.md

Beschrijf mogelijke services die studenten kunnen uitrollen, bijvoorbeeld:

* interne webserver;
* DNS;
* monitoringserver;
* loggingserver;
* reverse proxy;
* documentatieserver;
* eenvoudige identity/service-account-opzet;
* testclient.

Maak duidelijk dat elke service gedocumenteerd moet worden met doel, installatie, configuratie, firewallregels, back-up en testprocedure.

### docs/07-backup-en-restore.md

Beschrijf verwachtingen rond:

* back-upstrategie;
* wat er geback-upt wordt;
* retentie;
* restore-test;
* bewijs van restore;
* documentatie van mislukkingen en verbeteringen.

### docs/08-monitoring-en-logging.md

Beschrijf verwachtingen rond:

* monitoring van nodes;
* monitoring van services;
* dashboards;
* alerts;
* logging;
* incidentanalyse;
* minimale screenshots of exports in documentatie.

Voorzie opties zoals Zabbix, Grafana/Prometheus, Wazuh of andere lichte alternatieven, zonder één tool verplicht te maken tenzij nodig.

### docs/09-security-hardening.md

Beschrijf:

* SSH-hardening;
* updates;
* least privilege;
* firewallbeleid;
* logging;
* secrets management;
* certificaten;
* audit/checklist;
* wat absoluut verboden is.

### docs/10-documentatie-template.md

Maak een algemene handleiding voor goede technische documentatie:

* doel;
* context;
* stappen;
* validatie;
* rollback;
* screenshots;
* commando’s;
* testresultaten;
* veelgemaakte fouten;
* datum/auteur.

### templates

Maak bruikbare Markdown-templates voor:

* netwerkplan;
* server;
* service;
* firewallregel;
* back-uptest;
* incidentrapport;
* change request.

Templates moeten invulbaar zijn door studenten.

### praktische-afspraken.md

Werk praktische afspraken uit:

* aanwezigheid;
* groepswerk;
* zelfstandigheid;
* wekelijkse voortgang;
* rol van de docent;
* vragen via Issues;
* gebruik van GitHub;
* deadlines;
* verantwoordelijkheden binnen de groep.

Gebruik geen exacte lokalen of uurroosters tenzij als placeholder.

### spelregels.md

Maak duidelijke spelregels:

* geen toegang tot doos-Proxmox;
* geen onderliggende virtuele bekabeling aanpassen;
* geen OPNsense bypassen;
* geen campusnetwerk verstoren;
* geen DHCP op verkeerde netwerken;
* geen secrets in GitHub;
* geen destructieve acties zonder overleg;
* wijzigingen loggen;
* fouten melden;
* overtredingen kunnen gevolgen hebben voor evaluatie.

### github-werkwijze.md

Leg uit:

* Issues gebruiken voor taken;
* labels gebruiken;
* Pull Requests;
* commits;
* changelog;
* documentatie in Markdown;
* screenshots in images;
* diagrammen in diagrams;
* configs in configs zonder secrets;
* wanneer een issue gesloten mag worden.

### backlog.md

Maak een backlog met Must/Should/Could.

Gebruik deze thematische verdeling:

#### Iteration 1 – Oriëntatie en basisconnectiviteit

* omgeving verkennen;
* toegang controleren;
* netwerkplan opstellen;
* OPNsense basisconfig controleren;
* Proxmox-nodes bereikbaar maken;
* eerste documentatie.

#### Iteration 2 – Cluster en basisservices

* Proxmox-cluster vormen;
* storagekeuze documenteren;
* test-VM/container;
* DNS/DHCP/firewallregels;
* eerste interne service.

#### Iteration 3 – Security, backup en monitoring

* hardening;
* back-upstrategie;
* restore-test;
* monitoring;
* logging;
* incidentregistratie.

#### Iteration 4 – Stabilisatie, incidenten en eindoplevering

* verbeteringen;
* incidentopdracht;
* documentatie finaliseren;
* eindpresentatie;
* reflectie;
* demo.

### roadmap.md

Maak een weekplanning voor 12 weken, met duidelijke thema’s en deliverables. Houd het realistisch voor een eindvak.

### evaluatie.md

Maak een evaluatierubric. Gebruik bijvoorbeeld:

* Technische realisatie: 40%
* Documentatie en reproduceerbaarheid: 25%
* Operations, troubleshooting en incidentbeheer: 20%
* Samenwerking, communicatie en professionele houding: 15%

Werk per domein niveaus uit:

* uitstekend;
* goed;
* voldoende;
* onvoldoende;
* zwaar onvoldoende.

Maak duidelijk dat individuele bijdrage meetelt, ook bij groepswerk.

### eindoplevering.md

Beschrijf:

* wat de groep moet demonstreren;
* welke documenten klaar moeten zijn;
* welke tests getoond moeten worden;
* welke vragen studenten moeten kunnen beantwoorden;
* hoe de eindpresentatie opgebouwd wordt.

### supporttickets.md

Beschrijf hoe supporttickets werken:

* elk probleem wordt een issue;
* analyse;
* oplossing;
* validatie;
* documentatie;
* changelog;
* afsluiten.

### incidenten.md

Beschrijf hoe incidenten worden behandeld:

* detectie;
* impact;
* oorzaak;
* tijdelijke oplossing;
* definitieve oplossing;
* preventie;
* post-mortem.

### change-management.md

Beschrijf:

* wanneer een change request nodig is;
* risico-inschatting;
* uitvoeringsplan;
* rollbackplan;
* validatie;
* documentatie.

### groepsindeling.md

Maak een template waarin groepen hun gegevens invullen:

* groepsnummer;
* studenten;
* verantwoordelijkheden;
* IP-range;
* OPNsense-adres;
* Proxmox-node-adressen;
* services;
* links naar documentatie.

### .github/ISSUE_TEMPLATE

Maak GitHub issue templates in YAML-formaat voor:

* projecttaak;
* supportticket;
* incident;
* vraag;
* change request.

Zorg dat elk template studenten verplicht laat nadenken over:

* context;
* stappenplan;
* verwachte uitkomst;
* test/validatie;
* documentatie;
* risico/rollback waar relevant.

### .github/pull_request_template.md

Maak een PR-template met:

* samenvatting;
* gekoppelde issues;
* type wijziging;
* testbewijs;
* documentatie bijgewerkt ja/nee;
* bevat secrets ja/nee;
* reviewer checklist.

### .github/workflows/issue-changelog.yml

Maak een eenvoudige GitHub Action die bij het sluiten van een issue een changelog-entry toevoegt aan `changelog.md`.

Voorzie robuuste labelafhandeling. Ondersteun labels zoals:

* feature;
* fix;
* chore;
* docs;
* refactor;
* support;
* incident;
* change;
* question;
* must;
* should;
* could;
* other.

De workflow mag gebaseerd zijn op `actions/github-script`, maar zorg dat hij niet crasht als er geen comment is. In dat geval gebruikt hij de issue body of een standaardmelding.

### changelog.md

Maak een startbestand met korte uitleg dat wijzigingen automatisch of manueel bijgehouden worden.

## Belangrijke stijlrichtlijnen

* Schrijf alles in het Nederlands.
* Gebruik duidelijke Markdown.
* Gebruik praktische voorbeelden.
* Gebruik waarschuwingen waar studenten iets gevaarlijks kunnen doen.
* Vermijd te veel wollige tekst.
* Gebruik tabellen waar dat nuttig is.
* Gebruik checklists waar studenten iets moeten opleveren.
* Gebruik placeholders voor zaken die nog door de docent moeten worden ingevuld.
* Gebruik consequente bestandsnamen in lowercase met koppeltekens, behalve `README.md`.
* Zorg dat alle interne links werken.
* Voeg geen echte wachtwoorden, tokens, IP’s van bestaande infrastructuur of secrets toe.
* Voeg geen zware binaire bestanden toe.
* Maak geen fictieve screenshots.
* Maak geen installatiehandleiding die doet alsof exacte instellingen al bekend zijn wanneer die door de docent moeten worden ingevuld.
* Vermeld expliciet dat de exacte IP-ranges, logins en toegangsmethoden door de docent tijdens de start worden meegedeeld.

## Eindcontrole

Voer na het aanmaken van de repo deze controle uit:

1. Controleer of alle links tussen Markdown-bestanden kloppen.
2. Controleer of de repo bruikbaar is voor studenten die het vak voor het eerst openen.
3. Controleer of de nieuwe virtuele labo-opzet overal consequent gebruikt wordt.
4. Controleer of nergens staat dat studenten toegang krijgen tot de doos-Proxmox.
5. Controleer of nergens secrets of echte wachtwoorden staan.
6. Controleer of evaluatie, planning en verwachtingen duidelijk zijn.
7. Controleer of de GitHub issue templates en PR-template logisch bruikbaar zijn.
8. Geef op het einde een korte samenvatting van wat je hebt aangemaakt.
