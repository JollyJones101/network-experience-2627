# Netwerk- en dataflowplan

## Metadata

| Veld | Waarde |
|---|---|
| Groep/project | `<GROEP_EN_PROJECT>` |
| Proxmox-pool | `<POOL>` |
| Auteur/reviewer | `<NAMEN>` |
| Laatst bijgewerkt | `<DATUM>` |

## Netwerken

| Zone/VLAN | CIDR | Gateway | Doel | Beheerder |
|---|---|---|---|---|
| `<ZONE>` | `<CIDR>` | `<IP>` | `<DOEL>` | `<ROL>` |

## Workloads

| VMID | Hostnaam | Functie | IP/DNS | Luisterende poorten | Eigenaar |
|---:|---|---|---|---|---|
| `<ID>` | `<NAAM>` | `<FUNCTIE>` | `<WAARDE>` | `<POORTEN>` | `<ROL>` |

## Gegevensstromen

| Bron | Bestemming | Protocol/poort | Data | Authenticatie | Reden |
|---|---|---|---|---|---|
| `<BRON>` | `<DOEL>` | `<PROTO/POORT>` | `<CLASSIFICATIE>` | `<METHODE>` | `<WAAROM>` |

## Gedeelde wijzigingen

| Aanvraag | Eigenaar | Status | Change-issue |
|---|---|---|---|
| `<DNS_FIREWALL_PROXY_OF_ANDERS>` | `<ROL>` | `<STATUS>` | `<LINK>` |

## Diagram

`<LINK_NAAR_DIAGRAM>`

## Tests

- [ ] Bedoelde gebruikersflow werkt.
- [ ] Niet-toegelaten bron wordt geblokkeerd.
- [ ] Beheerpad werkt alleen voor beheerders.
- [ ] Datadienst is niet rechtstreeks voor gebruikers bereikbaar.
- [ ] Monitoring- en back-uppad werken.
- [ ] Onnodig uitgaand verkeer is beperkt.
- [ ] DNS, tijd en certificaat zijn gevalideerd.
