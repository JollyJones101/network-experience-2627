# Server template

## Metadata

| Veld | Waarde |
|---|---|
| Naam | `<SERVER_NAAM>` |
| Type | `<VM/LXC>` |
| Eigenaar | `<NAAM>` |
| Hostnode | `<PVE_NODE>` |
| Laatst bijgewerkt | `<DATUM>` |

## Doel

`<BESCHRIJF_DOEL>`

## Resources

| CPU | RAM | Disk | OS |
|---|---|---|---|
| `<CPU>` | `<RAM>` | `<DISK>` | `<OS>` |

## Netwerk

| Interface | Netwerk | IP | Gateway |
|---|---|---|---|
| `<IFACE>` | `<NETWERK>` | `<IP>` | `<GATEWAY>` |

## Beheer

- Beheeraccount: `<ACCOUNT_OF_ROL>`
- Secrets: `<SECRET_IN_BITWARDEN>`
- Firewallprofiel: `<SECURITY_GROUP>`

## Backup

`<BACKUP_AFSPRAAK>`

## Validatie

- [ ] Host bereikbaar.
- [ ] Service bereikbaar.
- [ ] Firewall getest.
- [ ] Backup getest indien relevant.

