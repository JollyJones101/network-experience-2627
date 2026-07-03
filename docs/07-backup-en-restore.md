# Backup en restore

Back-ups zijn pas waardevol wanneer restore getest is.

## Verwachtingen

Documenteer:

- wat geback-upt wordt;
- waar back-ups staan;
- retentie;
- frequentie;
- verantwoordelijke;
- restoreprocedure;
- testresultaten;
- mislukte tests en verbeteringen.

## Scope

Denk minstens aan:

- webshare-data;
- n8n-configuratie en workflows;
- belangrijke VM's/containers;
- OPNsense-configuratie-export zonder secrets waar mogelijk;
- documentatie in Git.

## Restore-test

Gebruik [templates/backup-test-template.md](templates/backup-test-template.md).

Minimale bewijsvoering:

- startstatus;
- uitgevoerde stappen;
- resultaat;
- screenshots/logs zonder secrets;
- lessons learned.

