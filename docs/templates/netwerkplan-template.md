# Netwerkplan template

## Metadata

| Veld | Waarde |
|---|---|
| Groep | `<GROEP_NUMMER>` |
| Auteur(s) | `<NAMEN>` |
| Laatst bijgewerkt | `<DATUM>` |
| Gekoppelde issues | `<ISSUES>` |

## Subnetten

| Netwerk | CIDR | Gateway | Doel |
|---|---|---|---|
| LAN | `<CIDR>` | `<IP>` | beheer en interne services |
| VPN | `<CIDR>` | `<IP>` | remote access |
| SDN VNet | `<CIDR>` | `<IP>` | interne VM/CT-segmentatie |

## Services

| Service | Host | IP | Poorten | Bereikbaarheid |
|---|---|---|---|---|
| `<SERVICE>` | `<HOST>` | `<IP>` | `<POORTEN>` | `<LAN/VPN/WAN>` |

## Firewallzones en regels

| Bron | Bestemming | Poort/protocol | Actie | Reden | Test |
|---|---|---|---|---|---|
| `<BRON>` | `<BESTEMMING>` | `<POORT>` | `<ALLOW/DENY>` | `<REDEN>` | `<BEWIJS>` |

## Diagram

Link naar diagram in `diagrams/`:

```text
<DIAGRAM_LINK>
```

## Testplan

- [ ] LAN-connectiviteit getest.
- [ ] DNS getest.
- [ ] VPN getest.
- [ ] Webshare getest.
- [ ] n8n getest.
- [ ] SDN-connectiviteit getest.
- [ ] Firewallblokkade getest.

