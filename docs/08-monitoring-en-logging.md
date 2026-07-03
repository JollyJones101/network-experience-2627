# Monitoring en logging

Monitoring en logging tonen dat jullie omgeving beheerd wordt, niet alleen geinstalleerd is.

## Verwachtingen

Voorzie zicht op:

- Proxmox-nodes;
- kritieke VM's/containers;
- webshare;
- n8n;
- VPN of remote access waar mogelijk;
- opslag en resourcegebruik;
- relevante logs.

## Mogelijke tools

- Uptime Kuma;
- Grafana/Prometheus als resources dat toelaten;
- Zabbix;
- Wazuh alleen als de resource-impact verantwoord is;
- lichte syslog-oplossing;
- ingebouwde Proxmox- en OPNsense-logs.

## Bewijs

Documenteer:

- dashboards of checks;
- alerts indien gebruikt;
- incidentanalyse;
- screenshots of exports zonder secrets;
- wat je doet bij een waarschuwing.

