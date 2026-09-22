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
| Beheeraccounts | Proxmox/applicatie | `<GROUP_VAULT_ITEM>` |
| Service-accounts | applicaties en automatisering | `<GROUP_VAULT_ITEM>` |
| Platformtoegang | Proxmox/beheerpad | `<GROUP_VAULT_ITEM_OF_DOOR_DOCENT_BEHEERD>` |
| Recovery | herstelcodes | `<GROUP_VAULT_ITEM>` |
