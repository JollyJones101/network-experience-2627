# Evaluatie

Network Experience wordt beoordeeld op technische realisatie, professioneel beheer en aantoonbare individuele bijdrage. Een configuratie die werkt maar niet uitgelegd, getest of gedocumenteerd is, is onvoldoende bewijs.

## Weging

| Domein | Gewicht |
|---|---:|
| Technische realisatie en integratie | 40% |
| Security, rechtenbeheer en netwerkafscherming | 20% |
| Documentatie, reproduceerbaarheid en change management | 20% |
| Operations, troubleshooting, monitoring en incidentbeheer | 10% |
| Samenwerking, communicatie en individuele bijdrage | 10% |

## Rubric

| Domein | Uitstekend | Goed | Voldoende | Onvoldoende | Zwaar onvoldoende |
|---|---|---|---|---|---|
| Technische realisatie en integratie | Alle verplichte onderdelen werken samen, met duidelijke keuzes en testbewijs. | Meeste onderdelen werken stabiel; kleine hiaten zijn verklaard. | Kernonderdelen werken, maar integratie of bewijs is beperkt. | Meerdere kernonderdelen ontbreken of werken onbetrouwbaar. | Geen bruikbare geintegreerde omgeving. |
| Security, rechtenbeheer en netwerkafscherming | Least privilege, VPN, OPNsense, Proxmox firewall, Bitwarden en secretsbeleid zijn consequent toegepast. | Security is grotendeels correct, met beperkte verbeterpunten. | Basisbeveiliging aanwezig, maar weinig diepgang of testbewijs. | Security is zwak, permissief of onvolledig. | Secretslekken, bypasses of gevaarlijke configuraties. |
| Documentatie en change management | Repo is volledig, reproduceerbaar en bruikbaar als technisch dossier. Changes en incidenten zijn correct gelogd. | Documentatie is duidelijk, maar mist enkele details of validaties. | Belangrijkste keuzes zijn beschreven, maar niet altijd reproduceerbaar. | Documentatie is fragmentarisch of achterhaald. | Nauwelijks documentatie of bewijs. |
| Operations en troubleshooting | Monitoring, logging, backup/restore en incidentanalyse tonen professioneel beheer. | Operations werken, maar zijn niet overal diep getest. | Minimale monitoring en backup zijn aanwezig. | Operations zijn oppervlakkig of niet aantoonbaar. | Geen aantoonbare beheerpraktijk. |
| Samenwerking en bijdrage | Issues, commits en presentatie tonen duidelijke individuele bijdrage en eigenaarschap. | Samenwerking is zichtbaar en evenwichtig genoeg. | Bijdrage is aantoonbaar, maar ongelijk of weinig expliciet. | Bijdrage is onduidelijk. | Geen aantoonbare individuele bijdrage. |

## Verplichte technische aandachtspunten

De evaluatie kijkt expliciet naar:

- Proxmox SDN;
- Proxmox user management met beperkte account;
- Bitwarden/password management;
- webshare-publicatie via OPNsense;
- n8n-workflow;
- Proxmox firewall/security groups;
- High Availability;
- VPN;
- back-up/restore-test;
- monitoring en logging;
- incident of change request;
- documentatie en bewijsvoering;
- respecteren van de RAM- en labo-beperkingen.

## Individuele bijdrage

Groepswerk betekent niet dat iedereen automatisch dezelfde beoordeling krijgt. De docent kan individuele vragen stellen over configuraties, keuzes, issues, commits en documentatie. Iedereen moet de eigen bijdrage kunnen uitleggen.

