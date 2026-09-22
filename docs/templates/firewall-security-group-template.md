# Firewall security group template

## Security group

| Veld | Waarde |
|---|---|
| Naam | `<SECURITY_GROUP>` |
| Laag | `<GEDEELD_NETWERK/PROXMOX/VM/HOST/APPLICATIE>` |
| Doel | `<DOEL>` |
| Eigenaar | `<NAAM>` |

## Regels

| Volgorde | Actie | Bron | Bestemming | Poort/protocol | Reden |
|---:|---|---|---|---|---|
| 1 | `<ALLOW/DENY>` | `<BRON>` | `<BESTEMMING>` | `<POORT>` | `<REDEN>` |

## IP sets

| Naam | Inhoud | Doel |
|---|---|---|
| `<IPSET>` | `<CIDR_OF_HOSTS>` | `<DOEL>` |

## Tests

- [ ] Toegelaten verkeer werkt.
- [ ] Ongewenst verkeer wordt geblokkeerd.
- [ ] Logging gecontroleerd.
- [ ] Regel is beperkt tot de bedoelde bron en bestemming.
- [ ] Tijdelijke regel heeft een eigenaar en vervaldatum.
- [ ] Documentatie bijgewerkt.
