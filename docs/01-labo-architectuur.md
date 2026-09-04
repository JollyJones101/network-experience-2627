# Labo-architectuur

Elke groep werkt in een eigen virtuele bedrijfsomgeving.

```text
Fysieke Proxmoxcluster opleiding
└── Doos-Proxmox groep X
    ├── OPNsense
    │   ├── WAN
    │   └── LAN
    ├── pve-x-01
    ├── pve-x-02
    └── pve-x-03
```

## Lagen

| Laag | Beheerder | Doel |
|---|---|---|
| Fysieke Proxmoxcluster | Docent/opleiding | Draait alle groepsomgevingen |
| Doos-Proxmox | Docent | Bevat de virtuele labocomponenten van een groep |
| OPNsense | Opleiding; studenten binnen changeproces | Edge firewall, router, NAT, VPN |
| Virtuele Proxmox-nodes | Opleiding voor basis; studenten voor eigen workloads | Werkend cluster voor VM's, containers, SDN, HA en firewall |
| VM's/containers | Studenten | Services en testomgevingen |

Studenten krijgen geen beheerrechten op de doos-Proxmox. Dat voorkomt dat groepen de onderliggende bekabeling aanpassen of OPNsense bypassen.

## Verkeerspad

Alle beheer- en serviceverkeer moet via OPNsense lopen.

```text
WAN/opleidingsnetwerk
        │
        ▼
    OPNsense
        │ LAN
        ▼
Proxmox-cluster en interne services
```

## IP-placeholders

Exacte IP-ranges worden door de docent bevestigd.

```text
Groep X LAN:       172.16.X.0/24
OPNsense LAN:     172.16.X.1
Proxmox node 1:   172.16.X.11
Proxmox node 2:   172.16.X.12
Proxmox node 3:   172.16.X.13
VPN-range:        <DOOR_DOCENT_BEVESTIGD>
SDN VNet:         <DOOR_GROEP_TE_KIEZEN>
```

## Relatie met Proxmox SDN

Maak onderscheid tussen:

- de onderliggende virtuele bekabeling van de docent;
- het LAN achter OPNsense;
- Proxmox SDN-netwerken binnen jullie cluster.

Proxmox SDN is een laag binnen jullie eigen cluster. Het vervangt niet de verplichte OPNsense-afscherming.

## Bestaande platformdiensten

Bij de start zijn de Proxmox-basisomgeving, automatische backups, reverse proxy, VPN, SSO en NetBox operationeel. Studenten bouwen deze niet opnieuw. Ze valideren de relevante paden voor hun workloads en gebruiken support- en changeprocedures wanneer de basis afwijkt of aangepast moet worden.

## Validatie van het verkeerspad

Documenteer minstens:

- default gateway van de Proxmox-nodes;
- traceroute of route-output;
- relevante OPNsense firewall/NAT-regels of een door de opleiding aangeleverd overzicht;
- test vanaf WAN/klaslokaalnetwerk naar een gepubliceerde service;
- screenshot of export zonder secrets.
