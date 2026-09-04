# Monitoring en logging

Monitoring en logging tonen dat jullie omgeving beheerd wordt, niet alleen geinstalleerd is.

## Algemene aandachtspunten

Monitoring kan zicht geven op:

- kritieke services;
- opslag en resourcegebruik;
- relevante logs.

Een bruikbare alert heeft een eigenaar, ernstniveau, drempel en reactieprocedure. SLI's en SLO's kunnen helpen om betrouwbaarheid meetbaar te maken.

## Mogelijke tools

- Uptime Kuma;
- Grafana/Prometheus als resources dat toelaten;
- Zabbix;
- Wazuh alleen als de resource-impact verantwoord is;
- lichte syslog-oplossing;
- ingebouwde Proxmox- en OPNsense-logs.

## Documentatie

Documenteer:

- dashboards of checks;
- alerts indien gebruikt;
- incidentanalyse;
- screenshots of exports zonder secrets;
- wat je doet bij een waarschuwing.
