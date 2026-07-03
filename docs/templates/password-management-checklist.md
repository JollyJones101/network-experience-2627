# Password management checklist

- [ ] Bitwarden of goedgekeurd alternatief is ingericht.
- [ ] Alle groepsleden hebben correcte toegang.
- [ ] Gedeelde wachtwoorden staan niet in GitHub.
- [ ] Service-accounts zijn opgenomen in de vault.
- [ ] Recovery codes staan veilig buiten GitHub.
- [ ] Toegang bij groepswissel is beschreven.
- [ ] Intrekken van toegang is beschreven.
- [ ] Screenshots zijn gecontroleerd op secrets.
- [ ] Configuratiebestanden zijn gecontroleerd op secrets.

## Categorieen secrets

| Categorie | Voorbeeld | Locatie |
|---|---|---|
| Beheeraccounts | Proxmox/OPNsense | `<GROUP_VAULT_ITEM>` |
| Service-accounts | webshare/n8n | `<GROUP_VAULT_ITEM>` |
| VPN | peers/keys | `<GROUP_VAULT_ITEM>` |
| Recovery | herstelcodes | `<GROUP_VAULT_ITEM>` |

