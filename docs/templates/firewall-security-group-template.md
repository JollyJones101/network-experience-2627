# Firewall security group template

## Security group

| Veld | Waarde |
|---|---|
| Naam | `<SECURITY_GROUP>` |
| Laag | `<CLUSTER/NODE/VM>` |
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
- [ ] Documentatie bijgewerkt.

