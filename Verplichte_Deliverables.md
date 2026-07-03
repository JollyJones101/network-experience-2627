## Verplichte technische deliverables

Voeg in de repository expliciet toe dat elke groep minstens de onderstaande onderdelen moet realiseren, documenteren, testen en verdedigen. Deze onderdelen zijn geen vrijblijvende uitbreidingen, maar maken deel uit van de kernopdracht van Network Experience.

Belangrijke beperking: elke groep beschikt over drie virtuele Proxmox-nodes met elk ongeveer **8 GB RAM**. De opdracht moet dus realistisch blijven. Vermijd zware enterprise-stacks. Gebruik waar mogelijk lichte Linux-VM’s, LXC-containers of Docker-containers. Maak duidelijk dat studenten keuzes moeten maken en niet onbeperkt services mogen stapelen.

### 1. Proxmox SDN

Elke groep moet Proxmox SDN gebruiken binnen hun virtuele Proxmox-cluster.

Verwachtingen:

* studenten maken minstens één Proxmox SDN-zone aan;
* studenten maken minstens één VNet aan;
* studenten documenteren waarvoor dit virtuele netwerk dient;
* studenten tonen aan welke VM’s/containers op welk netwerk zitten;
* studenten leggen uit wat het verschil is tussen:

  * de onderliggende virtuele bekabeling van de docent;
  * het LAN achter OPNsense;
  * de Proxmox SDN-netwerken binnen hun cluster;
* studenten testen connectiviteit tussen VM’s op het SDN-netwerk;
* studenten documenteren firewallregels die van toepassing zijn op dit netwerk.

Gebruik geen te complexe SDN-opzet zoals EVPN/VXLAN als dat niet nodig is. Een eenvoudige, begrijpbare SDN-opzet is voldoende, zolang studenten ze correct kunnen uitleggen.

Maak hiervoor een apart document:

```text
docs/11-proxmox-sdn.md
```

### 2. Volledig user management in Proxmox

Elke groep moet in Proxmox een correct gebruikers- en rechtenmodel uitwerken.

Verwachtingen:

* niet iedereen werkt permanent als `root`;
* er is minstens één beheerdersaccount voor de groep;
* er is minstens één beperkte account die zelf VM’s of containers kan aanmaken en verwijderen binnen een afgebakende scope;
* deze beperkte account mag niets doen met VM’s/containers van andere gebruikers of buiten de toegewezen pool;
* studenten gebruiken Proxmox-pools, rollen en ACL’s;
* studenten documenteren:

  * gebruikers;
  * rollen;
  * pools;
  * ACL-paden;
  * toegekende rechten;
  * testresultaten;
* studenten bewijzen met screenshots of teststappen dat de beperkte account:

  * een eigen VM/container kan aanmaken;
  * een eigen VM/container kan starten/stoppen;
  * een eigen VM/container kan verwijderen;
  * geen andere VM’s kan beheren;
  * geen clusterinstellingen kan aanpassen.

Maak duidelijk dat dit een kernonderdeel is van professioneel systeembeheer: least privilege, rollen, verantwoordelijkheid en controleerbaarheid.

Maak hiervoor een apart document:

```text
docs/12-proxmox-user-management.md
```

Voorzie ook een template:

```text
docs/templates/user-management-template.md
```

### 3. Password management met Bitwarden

Elke groep moet professioneel wachtwoordbeheer gebruiken.

Verwachtingen:

* elke groep gebruikt Bitwarden of een door de docent goedgekeurd alternatief;
* alle gedeelde wachtwoorden, service-accounts en recovery codes worden beheerd via de password manager;
* wachtwoorden worden nooit opgeslagen in GitHub, Markdown-bestanden, screenshots, tickets of configuratiebestanden;
* studenten spreken af wie toegang heeft tot welke secrets;
* studenten documenteren wel:

  * welke categorieën secrets bestaan;
  * wie toegang heeft;
  * hoe nieuwe wachtwoorden worden aangemaakt;
  * hoe wachtwoorden gedeeld worden;
  * wat gebeurt bij groepswissel of verlies van toegang;
  * hoe recovery geregeld is;
* studenten maken een duidelijk onderscheid tussen documentatie en secrets.

Belangrijk: de repository mag nooit echte wachtwoorden, tokens, private keys of recovery codes bevatten. Gebruik placeholders zoals:

```text
<SECRET_IN_BITWARDEN>
<GROUP_VAULT_ITEM>
```

Maak hiervoor een apart document:

```text
docs/13-password-management.md
```

Voorzie ook een checklist in:

```text
docs/templates/password-management-checklist.md
```

### 4. Webshare voor filesharing

Elke groep moet een webgebaseerde filesharing-service opzetten.

Doel: studenten moeten een interne of semi-publieke dienst veilig beschikbaar maken via OPNsense.

Verwachtingen:

* de groep kiest een lichte filesharing-oplossing, bijvoorbeeld:

  * File Browser;
  * SFTPGo;
  * eenvoudige WebDAV-service;
  * andere lichte oplossing mits motivatie;
* zware oplossingen zoals Nextcloud mogen alleen als de groep kan aantonen dat dit haalbaar is binnen de RAM-limieten;
* de webshare moet bereikbaar zijn vanaf de WAN-kant van OPNsense, bijvoorbeeld vanuit het klaslokaalnetwerk;
* indien echte internetpublicatie niet mogelijk of niet gewenst is, volstaat bereikbaarheid vanuit het klaslokaalnetwerk of het opleidingsnetwerk;
* toegang moet beveiligd zijn met accounts;
* anonieme write-access is verboden;
* studenten documenteren:

  * gekozen software;
  * installatie;
  * netwerkpad;
  * firewallregels;
  * NAT/port forward of reverse proxy;
  * authenticatie;
  * testprocedure;
  * risicoanalyse;
  * back-up van gedeelde bestanden;
* studenten testen upload, download en toegangscontrole.

Maak duidelijk dat het niet alleen gaat om “een share online krijgen”, maar om een veilige publicatie van een dienst achter een firewall.

Maak hiervoor een apart document:

```text
docs/14-webshare.md
```

Voorzie ook een service-template dat hiervoor bruikbaar is.

### 5. n8n-automatisatie

Elke groep moet minstens één automatisatie realiseren met n8n.

Gezien de beperkte RAM moet n8n licht opgezet worden, bijvoorbeeld via Docker met SQLite, tenzij de groep goed motiveert waarom een andere setup nodig is.

Verwachtingen:

* n8n draait als interne service binnen de groepsomgeving;
* n8n is niet onbeveiligd publiek bereikbaar;
* toegang verloopt via accounts en indien nodig via VPN of afgeschermde firewallregels;
* studenten bouwen minstens één zinvolle workflow;
* de workflow moet passen binnen systeem- of netwerkbeheer.

Voorbeelden van toegelaten workflows:

* periodieke controle of de webshare bereikbaar is;
* melding/log bij falende healthcheck;
* automatische registratie van een incident in een bestand of webhook;
* eenvoudige back-upcontrole;
* notificatie wanneer een service down is;
* automatische documentatie-update via een gecontroleerde workflow;
* periodieke export of statusrapport.

Verwachtingen rond documentatie:

* doel van de workflow;
* trigger;
* stappen;
* gebruikte credentials;
* waar credentials veilig bewaard worden;
* testresultaat;
* foutafhandeling;
* beveiligingsrisico’s;
* screenshots of export zonder secrets.

Maak hiervoor een apart document:

```text
docs/15-n8n-automatisatie.md
```

Voorzie ook een template:

```text
docs/templates/n8n-workflow-template.md
```

### 6. Proxmox firewalling met security groups

Elke groep moet de Proxmox-firewall gebruiken, niet alleen de firewall in OPNsense.

Verwachtingen:

* Proxmox firewall wordt geactiveerd waar nodig;
* studenten gebruiken security groups;
* studenten gebruiken IP sets waar zinvol;
* studenten maken regels op cluster-, node- of VM-niveau waar passend;
* studenten documenteren het verschil tussen:

  * OPNsense firewall;
  * Proxmox firewall;
  * firewall binnen een VM/container;
* studenten tonen aan dat ongewenst verkeer geblokkeerd wordt;
* studenten tonen aan dat toegelaten verkeer blijft werken;
* studenten documenteren minstens:

  * management access;
  * webshare access;
  * n8n access;
  * inter-VM traffic;
  * monitoring traffic;
  * backup traffic indien van toepassing.

Maak duidelijk dat firewallregels niet enkel “allow all” mogen zijn. Studenten moeten kunnen uitleggen waarom verkeer wel of niet toegelaten wordt.

Maak hiervoor een apart document:

```text
docs/16-proxmox-firewall-security-groups.md
```

Voorzie ook een template:

```text
docs/templates/firewall-security-group-template.md
```

### 7. High Availability

Elke groep moet High Availability in Proxmox opzetten en testen, binnen de beperkingen van de nested labo-omgeving.

Belangrijke nuance: omdat dit een virtuele en beperkte labo-omgeving is met drie Proxmox-VM’s van elk ongeveer 8 GB RAM, wordt geen zware productie-HA verwacht. Het doel is dat studenten het concept begrijpen, correct configureren en de beperkingen kunnen uitleggen.

Verwachtingen:

* studenten activeren/configureren Proxmox HA;
* studenten kiezen één kleine test-VM of test-container als HA-resource;
* studenten documenteren welke storage gebruikt wordt;
* studenten leggen uit of echte automatische failover mogelijk is met hun storagekeuze;
* studenten testen een gecontroleerd scenario, bijvoorbeeld:

  * node maintenance;
  * VM migratie;
  * stop/start via HA;
  * gesimuleerde node-uitval indien veilig toegestaan;
* studenten documenteren:

  * HA group;
  * resource;
  * prioriteiten;
  * failoververwachting;
  * testresultaten;
  * beperkingen;
  * risico’s.

Maak expliciet dat studenten niet mogen doen alsof dit een volwaardige productie-HA-oplossing is als de storage of nested omgeving dat niet ondersteunt. Correct uitleggen waarom iets beperkt werkt is beter dan fout beweren dat het volledig productiegeschikt is.

Maak hiervoor een apart document:

```text
docs/17-high-availability.md
```

Voorzie ook een template:

```text
docs/templates/ha-test-template.md
```

### 8. VPN opzetten

Elke groep moet VPN-toegang voorzien tot hun omgeving.

Verwachtingen:

* de VPN draait bij voorkeur op OPNsense;
* WireGuard is aanbevolen, OpenVPN mag indien gemotiveerd;
* VPN-toegang geeft toegang tot de interne beheeromgeving;
* VPN-gebruikers krijgen alleen toegang tot wat nodig is;
* studenten documenteren:

  * VPN-type;
  * adresrange;
  * toegelaten routes;
  * firewallregels;
  * gebruikers of peers;
  * testprocedure;
  * intrekken van toegang;
  * risico’s;
* studenten testen toegang tot minstens:

  * Proxmox webinterface;
  * webshare;
  * n8n indien van toepassing;
  * monitoring of een interne testservice.

Maak duidelijk dat VPN niet gewoon “aanzetten” is, maar deel uitmaakt van remote access management.

Maak hiervoor een apart document:

```text
docs/18-vpn.md
```

Voorzie ook een template:

```text
docs/templates/vpn-test-template.md
```

## Aanvullende aanbevolen onderdelen

Naast de verplichte onderdelen mogen studenten extra services toevoegen, zolang ze binnen de beschikbare resources blijven en goed gedocumenteerd worden.

Stel in de repo enkele lichte opties voor:

* Uptime Kuma voor eenvoudige monitoring;
* Homepage of Dashy als intern dashboard;
* Caddy, Nginx Proxy Manager of Traefik als reverse proxy;
* Prometheus + Grafana alleen als de groep de resource-impact kan verantwoorden;
* eenvoudige DNS-service;
* interne documentatiesite;
* eenvoudige Linux testclient;
* Ansible voor beperkte automatisatie;
* back-upscript met cron/systemd timer;
* logcollectie met een lichte syslog-oplossing.

Waarschuw expliciet voor te zware keuzes binnen deze labo-omgeving:

* volledige Kubernetes-clusters;
* zware Nextcloud-installaties;
* meerdere Windows Servers;
* grote databases;
* uitgebreide SIEM-stacks;
* alles tegelijk draaien zonder resourceplanning.

## Aanpassing van de evaluatie

Verwerk bovenstaande verplichte onderdelen in `evaluatie.md`.

Gebruik deze aangepaste evaluatieverdeling:

* Technische realisatie en integratie: 40%
* Security, rechtenbeheer en netwerkafscherming: 20%
* Documentatie, reproduceerbaarheid en change management: 20%
* Operations, troubleshooting, monitoring en incidentbeheer: 10%
* Samenwerking, communicatie en individuele bijdrage: 10%

Zorg dat de evaluatierubric expliciet punten bevat voor:

* Proxmox SDN;
* Proxmox user management met beperkte account;
* Bitwarden/password management;
* webshare-publicatie via OPNsense;
* n8n-workflow;
* Proxmox firewall/security groups;
* High Availability;
* VPN;
* documentatie en bewijsvoering;
* respecteren van de RAM- en labo-beperkingen.

Maak duidelijk dat een werkende oplossing zonder correcte uitleg, documentatie of securityconfiguratie niet automatisch voldoende is.

## Aanpassing van de roadmap

Verwerk de verplichte onderdelen in een realistische planning van 12 weken.

Gebruik bijvoorbeeld:

### Week 1 – Oriëntatie en toegang

* labo-architectuur begrijpen;
* toegang tot OPNsense en Proxmox-nodes testen;
* groepsrollen vastleggen;
* Bitwarden-vault of password management-afspraken opzetten;
* eerste netwerkplan.

### Week 2 – Basisnetwerk en OPNsense

* LAN/WAN controleren;
* IP-plan finaliseren;
* basisfirewall;
* NAT;
* bewijs dat alles achter OPNsense zit.

### Week 3 – Proxmox-cluster

* cluster vormen;
* node naming;
* storagekeuze;
* test-VM/container.

### Week 4 – Proxmox SDN

* SDN-zone;
* VNet;
* testconnectiviteit;
* documentatie.

### Week 5 – User management en rechten

* gebruikers;
* rollen;
* pools;
* beperkte VM-beheeraccount;
* rechten testen.

### Week 6 – Webshare

* filesharing-service;
* firewall/NAT/reverse proxy;
* toegangscontrole;
* back-upafspraak.

### Week 7 – VPN

* VPN op OPNsense;
* remote access;
* gebruikers/peers;
* firewallregels;
* testbewijs.

### Week 8 – Proxmox firewall en security groups

* Proxmox firewall;
* security groups;
* IP sets;
* test toegelaten/geblokkeerd verkeer.

### Week 9 – n8n-automatisatie

* n8n installeren;
* workflow bouwen;
* credentials veilig beheren;
* workflow testen.

### Week 10 – High Availability

* HA configureren;
* kleine testresource;
* failover/migratie-test;
* beperkingen documenteren.

### Week 11 – Monitoring, backup en incident

* monitoring;
* logging;
* back-up en restore-test;
* incidentrapport.

### Week 12 – Stabilisatie en eindoplevering

* documentatie finaliseren;
* demo voorbereiden;
* eindpresentatie;
* individuele technische bevraging.

## Aanpassing van de repositorystructuur

Voeg deze bestanden toe bovenop de eerder gevraagde structuur:

```text
docs/11-proxmox-sdn.md
docs/12-proxmox-user-management.md
docs/13-password-management.md
docs/14-webshare.md
docs/15-n8n-automatisatie.md
docs/16-proxmox-firewall-security-groups.md
docs/17-high-availability.md
docs/18-vpn.md
docs/templates/user-management-template.md
docs/templates/password-management-checklist.md
docs/templates/n8n-workflow-template.md
docs/templates/firewall-security-group-template.md
docs/templates/ha-test-template.md
docs/templates/vpn-test-template.md
```

Update ook:

```text
README.md
roadmap.md
evaluatie.md
backlog.md
spelregels.md
praktische-afspraken.md
eindoplevering.md
docs/01-labo-architectuur.md
docs/04-proxmox-cluster.md
docs/05-netwerkplan.md
docs/06-services.md
docs/09-security-hardening.md
```

zodat deze verplichte onderdelen overal consequent vermeld worden.

## Minimale einddemo

Elke groep moet op het einde minstens demonstreren:

1. toegang via VPN;
2. OPNsense als verplichte gateway;
3. Proxmox-cluster met drie nodes;
4. Proxmox SDN met minstens één werkend VNet;
5. beperkte Proxmox-account die alleen eigen VM’s/containers kan beheren;
6. Bitwarden/password management-afspraken zonder secrets in GitHub;
7. webshare bereikbaar via de WAN-kant of klaslokaalnetwerk;
8. n8n-workflow die aantoonbaar werkt;
9. Proxmox firewall met security groups;
10. HA-configuratie met testresource;
11. back-up/restore-test;
12. technische documentatie en changelog;
13. incident of change request met correcte opvolging.

Zorg dat de repo studenten duidelijk maakt dat de opdracht niet enkel gaat om installeren, maar om professioneel beheren, beveiligen, documenteren en kunnen uitleggen.
