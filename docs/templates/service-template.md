# Service template

## Metadata

| Veld | Waarde |
|---|---|
| Service | `<SERVICE_NAAM>` |
| Eigenaar | `<NAAM>` |
| Host | `<HOST>` |
| Laatst bijgewerkt | `<DATUM>` |
| Gekoppelde issues | `<ISSUES>` |

## Doel

`<WAAROM_BESTAAT_DEZE_SERVICE>`

## Installatie

```text
<STAPPEN_OF_LINK_NAAR_SCRIPT>
```

## Configuratie

Beschrijf instellingen zonder secrets.

## Netwerkpad

```text
Client -> bestaande VPN/reverse proxy -> OPNsense -> <SERVICE>
```

## Firewallregels

| Laag | Regel | Reden |
|---|---|---|
| OPNsense | `<REGEL>` | `<REDEN>` |
| Proxmox | `<REGEL>` | `<REDEN>` |
| Host | `<REGEL>` | `<REDEN>` |

## Authenticatie

- Accountmodel: `<BESCHRIJVING>`
- Secrets: `<SECRET_IN_BITWARDEN>`

## Backup

`<BACKUP_EN_RESTORE>`

## Testprocedure

- [ ] Bereikbaarheid getest.
- [ ] Authenticatie getest.
- [ ] Ongewenste toegang geblokkeerd.
- [ ] Backup of export getest.
