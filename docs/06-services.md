# Services

Elke service moet bewust gekozen, licht genoeg en professioneel gedocumenteerd zijn.

## Verplichte services

- webshare: zie [14-webshare.md](14-webshare.md);
- n8n: zie [15-n8n-automatisatie.md](15-n8n-automatisatie.md);
- monitoring/logging: zie [08-monitoring-en-logging.md](08-monitoring-en-logging.md).
- Minecraft-server voor de opleiding: zie [19-minecraft-server.md](19-minecraft-server.md).

## Mogelijke extra services

- interne webserver;
- DNS;
- Uptime Kuma;
- Homepage of Dashy;
- Caddy, Nginx Proxy Manager of Traefik;
- eenvoudige documentatieserver;
- Linux testclient;
- Ansible voor beperkte automatisatie;
- licht back-upscript met cron/systemd timer;
- lichte syslog-oplossing.

## Minecraft-server

De Minecraft-server is een verplichte, langlopende opleidingsservice. De volledige opdracht, inclusief BlueMap, hub, security, rollen, optimalisatie en overdracht, staat in [19-minecraft-server.md](19-minecraft-server.md). Houd de installatie licht en plan het resourcegebruik naast de andere verplichte services.

## Vermijd zware keuzes

- volledige Kubernetes-clusters;
- zware Nextcloud-installaties zonder resourcebewijs;
- meerdere Windows Servers;
- grote databases;
- uitgebreide SIEM-stacks;
- te veel services tegelijk.

## Documentatie per service

Gebruik [templates/service-template.md](templates/service-template.md). Beschrijf minstens:

- doel;
- eigenaar;
- installatie;
- configuratie;
- netwerkpad;
- firewallregels;
- authenticatie;
- back-up;
- monitoring;
- testprocedure;
- rollback.
