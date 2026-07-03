# n8n-automatisatie

Elke groep realiseert minstens een zinvolle automatisatie met n8n.

## Randvoorwaarden

- n8n draait als interne service.
- Gebruik een lichte setup, bijvoorbeeld Docker met SQLite.
- n8n is niet onbeveiligd publiek bereikbaar.
- Credentials worden veilig beheerd in Bitwarden of n8n credentials, niet in GitHub.

## Voorbeelden

- periodieke controle of webshare bereikbaar is;
- melding/log bij falende healthcheck;
- automatische registratie van een incident in bestand of webhook;
- eenvoudige back-upcontrole;
- notificatie wanneer een service down is;
- periodieke statusrapportage.

## Documentatie

Gebruik [templates/n8n-workflow-template.md](templates/n8n-workflow-template.md).

Beschrijf:

- doel;
- trigger;
- stappen;
- credentials en veilige opslag;
- testresultaat;
- foutafhandeling;
- beveiligingsrisico's;
- screenshot of export zonder secrets.

