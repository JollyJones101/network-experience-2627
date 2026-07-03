# Spelregels

Deze spelregels beschermen de labo-omgeving, het opleidingsnetwerk en de evaluatiekwaliteit.

## Absoluut niet toegestaan

- Inloggen op of wijzigen aan de onderliggende doos-Proxmox.
- Virtuele bekabeling aanpassen zonder toestemming.
- OPNsense bypassen door nodes of services rechtstreeks op WAN te hangen.
- Het campusnetwerk of opleidingsnetwerk verstoren.
- DHCP aanbieden op netwerken waar dat niet expliciet mag.
- Wachtwoorden, tokens, private keys, certificaatsleutels of recovery codes in GitHub plaatsen.
- Destructieve acties uitvoeren zonder rollbackplan of overleg.
- Securityregels vervangen door "allow all" zonder motivatie en test.

Overtredingen kunnen gevolgen hebben voor de evaluatie.

## Verplicht

- Alle beheerwijzigingen worden gelogd via issues, commits, change requests of documentatie.
- Fouten en incidenten worden gemeld. Fouten maken mag; fouten verzwijgen niet.
- Alle verkeer van de omgeving loopt via OPNsense.
- Secrets worden beheerd via Bitwarden of een door de docent goedgekeurd alternatief.
- Beperkte Proxmox-accounts worden getest en gebruikt waar passend.
- Firewallregels worden gemotiveerd en getest.
- Exacte IP-ranges, logins en toegangsmethoden worden door de docent bevestigd.

## Veilig testen

Gebruik gecontroleerde testscenario's. Simuleer uitval of destructieve acties alleen als dat veilig is en binnen de opdracht past. Noteer vooraf:

- doel van de test;
- impact;
- rollbackplan;
- verwachte uitkomst;
- validatie.

