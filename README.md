# Network Experience

Welkom bij **Network Experience**, het afsluitende netwerk- en systeembeheervak voor studenten Elektronica-ICT, afstudeerrichting ICT.

In dit vak beheer je met je groep een kleine bedrijfsomgeving. Je krijgt geen volledig stappenplan dat je blind volgt. Je onderzoekt, beslist, configureert, test, documenteert en verdedigt je keuzes zoals je dat in een professionele beheercontext zou doen.

## Deze repo als groepsblueprint

Elke groep clone't of fork't deze repository en gebruikt ze als eigen werkruimte.

```text
1. Maak een groepsrepo op basis van deze blueprint.
2. Vul alle documentatie aan met jullie eigen omgeving.
3. Gebruik issues voor taken, vragen, support, incidenten en changes.
4. Bewaar diagrammen in diagrams/ en screenshots in images/.
5. Bewaar configuratievoorbeelden in configs/, maar nooit secrets.
6. Zorg dat de repo op het einde jullie technische bewijsdossier is.
```

Wat niet gedocumenteerd, getest of gelogd is, telt beperkt of niet mee.

## Waarop werken jullie?

Elke groep krijgt een eigen virtuele labo-omgeving:

```text
Fysieke Proxmoxcluster opleiding
└── Doos-Proxmox groep X
    ├── OPNsense
    │   ├── WAN: verbinding naar buiten/opleidingsnetwerk
    │   └── LAN: intern groepsnetwerk
    ├── pve-x-01
    ├── pve-x-02
    └── pve-x-03
```

De docent beheert de fysieke Proxmoxcluster en de onderliggende doos-Proxmox. Studenten krijgen daar geen beheerrechten op.

De hardware, de Proxmox-basisomgeving, automatische backups, reverse proxy, VPN, SSO en NetBox zijn bij de start operationeel. Jullie bouwen die onderdelen niet opnieuw. Jullie gebruiken en valideren ze, melden afwijkingen en beheren de workloads die jullie erop plaatsen.

Jullie beheren binnen de afgesproken scope:

- toegewezen netwerk-, rechten- en firewallconfiguratie voor de eigen workloads;
- toegewezen resources op het Proxmox-cluster;
- VM's, containers, netwerken en services binnen jullie cluster;
- documentatie, changes, incidenten en bewijsvoering.

Alle verkeer van de Proxmox-nodes en services moet via OPNsense verlopen. De onderliggende virtuele bekabeling mag niet aangepast of omzeild worden.

## Project kiezen

Alle mogelijke studentenprojecten staan uitsluitend in [backlog.md](backlog.md). Kies samen met de docent één haalbaar project en maak daarna issues voor ontwerp, uitvoering, tests, documentatie en overdracht.

De omgeving is beperkt: reken op drie virtuele Proxmox-nodes met ongeveer 8 GB RAM per node. Kies dus bewust voor lichte VM's, LXC-containers of Docker-containers. Zware enterprise-stacks zijn alleen verdedigbaar als je resource-impact correct aantoont.

## Start hier

Begin met [docs/00-start-here.md](docs/00-start-here.md).

Lees daarna zeker:

- [praktische-afspraken.md](praktische-afspraken.md)
- [spelregels.md](spelregels.md)
- [github-werkwijze.md](github-werkwijze.md)
- [roadmap.md](roadmap.md)
- [evaluatie.md](evaluatie.md)

## Evaluatie in het kort

De evaluatie kijkt niet alleen naar "het werkt".

| Domein | Gewicht |
|---|---:|
| Technische realisatie en integratie | 30% |
| Security, rechtenbeheer en netwerkafscherming | 20% |
| Automatisering en reproduceerbaarheid | 15% |
| Operations, observability en resilience | 20% |
| Documentatie, samenwerking en individuele bijdrage | 15% |

Een werkende oplossing zonder correcte uitleg, documentatie, securityconfiguratie of testbewijs is niet automatisch voldoende.

## Geen secrets in GitHub

Plaats nooit wachtwoorden, tokens, private keys, certificaatsleutels, recovery codes of echte gedeelde credentials in deze repository. Gebruik placeholders zoals:

```text
<SECRET_IN_BITWARDEN>
<GROUP_VAULT_ITEM>
```
