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

## Wat bouwen jullie?

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

Jullie beheren wel:

- OPNsense;
- de drie virtuele Proxmox-nodes;
- het Proxmox-cluster;
- VM's, containers, netwerken en services binnen jullie cluster;
- documentatie, changes, incidenten en bewijsvoering.

Alle verkeer van de Proxmox-nodes en services moet via OPNsense verlopen. De onderliggende virtuele bekabeling mag niet aangepast of omzeild worden.

## Verplichte kernonderdelen

Elke groep realiseert, documenteert, test en verdedigt minstens:

- Proxmox-cluster met drie nodes;
- Proxmox SDN met minstens een zone en VNet;
- Proxmox user management met rollen, pools en beperkte account;
- professioneel password management met Bitwarden of goedgekeurd alternatief;
- webshare die veilig bereikbaar is via de WAN-kant of het opleidingsnetwerk;
- n8n-automatisatie voor een zinvolle beheerworkflow;
- Proxmox firewall met security groups en IP sets waar zinvol;
- High Availability met een kleine testresource;
- VPN-toegang tot de interne beheeromgeving;
- back-up en restore-test;
- monitoring, logging, incidenten en change management.
- een duurzame Minecraft-server voor de opleiding met BlueMap, een beschermde hub, rolverdeling, optimalisatie en overdracht: zie [docs/19-minecraft-server.md](docs/19-minecraft-server.md).

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
| Technische realisatie en integratie | 40% |
| Security, rechtenbeheer en netwerkafscherming | 20% |
| Documentatie, reproduceerbaarheid en change management | 20% |
| Operations, troubleshooting, monitoring en incidentbeheer | 10% |
| Samenwerking, communicatie en individuele bijdrage | 10% |

Een werkende oplossing zonder correcte uitleg, documentatie, securityconfiguratie of testbewijs is niet automatisch voldoende.

## Geen secrets in GitHub

Plaats nooit wachtwoorden, tokens, private keys, certificaatsleutels, recovery codes of echte gedeelde credentials in deze repository. Gebruik placeholders zoals:

```text
<SECRET_IN_BITWARDEN>
<GROUP_VAULT_ITEM>
```
