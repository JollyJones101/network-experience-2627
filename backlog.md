# Mogelijke studentenprojecten

Kies in overleg met de docent één project dat past binnen de beschikbare resources. De hardware, Proxmox-basis, automatische backups, reverse proxy, VPN, SSO en NetBox zijn al aanwezig en hoeven niet opnieuw gebouwd te worden.

| Project | Korte uitleg |
|---|---|
| Minecraft-communityserver | Bouw één blijvende server voor alle studiejaren en docenten, met BlueMap, een hub, rollen en duidelijke moderatie. |
| n8n-automatisaties | Automatiseer nuttige beheertaken zoals healthchecks, meldingen, accountreviews of ticketregistratie. |
| Homepage of Heimdall | Maak een verzorgd startportaal met links, statusinformatie en documentatie van alle opleidingsdiensten. |
| Uptime Kuma-statuspagina | Monitor belangrijke services en toon storingen en gepland onderhoud op een centrale statuspagina. |
| Monitoringdashboard | Verzamel systeem- en servicemetrics en visualiseer ze met bijvoorbeeld Grafana en Prometheus. |
| Centrale logging | Verzamel logs van meerdere systemen met bijvoorbeeld Loki, Graylog of een lichte syslogoplossing. |
| Documentatieportaal | Publiceer technische documentatie met MkDocs, BookStack of Wiki.js. |
| Gitea en CI/CD | Voorzie een lichte Git-omgeving en automatiseer tests of deployments via een pipeline. |
| Ansible-beheer | Automatiseer installatie, configuratie en updates van meerdere Linux-systemen. |
| GitOps-deployment | Beheer de configuratie en deployment van een service reproduceerbaar vanuit Git. |
| Webshare | Bouw een veilige filesharingdienst met accounts, quota's en gecontroleerde externe toegang. |
| Vaultwarden | Voorzie een intern platform voor veilig beheer en delen van servicecredentials. |
| DNS-filtering | Blokkeer ongewenste domeinen en verzamel bruikbare statistieken met Pi-hole of AdGuard Home. |
| Container registry | Bouw een private registry voor gecontroleerde opslag en distributie van containerimages. |
| CTF-platform | Richt een kleine, geïsoleerde omgeving in met securitychallenges voor medestudenten. |
| Ticketsysteem | Bouw een portaal voor supportvragen, incidenten en wijzigingsaanvragen. |
| Reservatiesysteem | Maak een kleine toepassing waarmee studenten laboapparatuur of tijdsloten kunnen reserveren. |
| Selfserviceportaal | Laat gebruikers veilige, beperkte acties aanvragen of uitvoeren zonder volledige beheerrechten. |
| Capaciteitsdashboard | Meet CPU, RAM en opslaggroei en maak een onderbouwde capaciteitsplanning. |
| High-availabilityproef | Test gecontroleerd wat er gebeurt wanneer een node of kleine workload uitvalt. |
| Honeypot | Plaats na toestemming een sterk geïsoleerde honeypot en analyseer uitsluitend het toegelaten verkeer. |
| Eigen voorstel | Stel een ander project voor met een duidelijk doel, gebruikers, scope en haalbaar resourcebudget. |

Elk gekozen project gebruikt waar relevant de bestaande reverse proxy, VPN, SSO, NetBox en backupvoorziening. Documenteer het ontwerp, de verantwoordelijken, de beveiliging, de testprocedure en de overdracht naar een volgende groep.
