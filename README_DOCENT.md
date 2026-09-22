# Docentenhandleiding: Smith voorbereiden

Deze repository gaat uit van één gedeelde Proxmox-productienode, **Smith**. Studenten mogen binnen een afgebakende pool VM's aanmaken en beheren. Ze krijgen geen rechten op hostconfiguratie, storagebeheer, clusterinstellingen of workloads van andere groepen.

## Voor de projectstart

Leg per groep minstens deze gegevens vast:

| Onderdeel | Voorbeeld |
|---|---|
| Proxmox-pool | `nx-groep-01` |
| Proxmox-rol | VM-beheer binnen de eigen pool, geen hostbeheer |
| VMID-range | `1100–1199` |
| VLAN/subnet | door de opleiding toegewezen |
| Resourcebudget | vCPU, RAM en disk als groepsmaximum |
| DNS/reverse proxy | aanvraagprocedure en naamconventie |
| Back-up | beschikbare job, retentie en uitzonderingen |
| Beheerpad | campusnetwerk en/of VPN |
| Publieke toegang | standaard uit; alleen na expliciete goedkeuring |

## Minimale technische voorbereiding

- Maak één pool en één beperkte groep/rol per studentengroep.
- Koppel alleen de toegelaten netwerkbridge(s) of VLANs.
- Dwing een herkenbare naamconventie en VMID-range af.
- Reserveer resources; vermijd dat één groep Smith kan uitputten.
- Voorzie een veilige route voor beheer, DNS- en tijdsynchronisatie.
- Leg vast hoe studenten firewall-, DNS-, certificaat- en reverse-proxywijzigingen aanvragen.
- Controleer back-upvensters en beschikbare restorecapaciteit.
- Maak een noodprocedure voor misbruik, resource-uitputting en kwetsbare publieke diensten.

Gebruik [docs/docent/docent-checklist.md](docs/docent/docent-checklist.md) voor intake, tussentijdse controles en de eindoplevering.

## Projecttoewijzing

De [projectcatalogus](projecten/README.md) bevat tien grote opdrachten. Wijs projecten toe op basis van groepsgrootte, beschikbare capaciteit en afhankelijkheden. Leg per groep de verplichte onderdelen en maximaal toegestane uitbreidingen vast in het projectcharter.

Voor de LAN-party zijn goedkeuring door Stuvo, lokaalbeheer en IT/netwerkbeheer expliciete go/no-govoorwaarden. Zonder schriftelijke toestemming organiseert de groep een tabletopoefening en een kleinschalige technische proef in een toegelaten lokaal; ze sluit nooit eigen netwerkapparatuur aan op het campusnetwerk zonder akkoord.

## Aanbevolen gates

| Gate | Uiterlijk | Beslissing |
|---|---:|---|
| Charter | week 2 | doelgroep, scope en eigenaar goedgekeurd |
| Architectuur | week 4 | netwerk, security en resources haalbaar |
| Productie-intake | week 7 | minimale security en beheerbaarheid aanwezig |
| Gebruikerstest | week 10 | dienst veilig bruikbaar voor testpubliek |
| Overdracht | week 12 | runbooks, restoretest en eigenaarschap rond |

Bij elke gate kan de docent scope verkleinen, publicatie uitstellen of een onveilige dienst laten uitschakelen.
