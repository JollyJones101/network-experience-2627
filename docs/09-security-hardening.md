# Security hardening

Security is een kernonderdeel van de opdracht.

## Verwachtingen

- Updates plannen en documenteren.
- SSH hardenen waar gebruikt.
- Least privilege toepassen.
- Proxmox user management gebruiken.
- Bitwarden of goedgekeurd alternatief gebruiken.
- VPN-toegang beperken.
- OPNsense en Proxmox firewall combineren.
- Logging controleren.
- Certificaten en keys veilig beheren.
- Geen secrets in GitHub.

## Checklist

- [ ] Rootgebruik beperkt.
- [ ] Beperkte Proxmox-account getest.
- [ ] Pools en ACL's gedocumenteerd.
- [ ] OPNsense-regels gemotiveerd.
- [ ] Proxmox security groups gebruikt.
- [ ] Webshare heeft authenticatie.
- [ ] n8n is niet onbeveiligd publiek bereikbaar.
- [ ] VPN-users/peers zijn beheerd.
- [ ] Secrets staan in Bitwarden.
- [ ] Backups en exports bevatten geen zichtbare secrets.

## Verboden

- `allow all` als blijvende firewallstrategie.
- Anonieme write-access op webshare.
- Onbeveiligde publieke n8n.
- Private keys of recovery codes in repo.
- Bypass van OPNsense.

