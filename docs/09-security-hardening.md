# Security hardening

Security geldt voor elk gekozen project.

## Verwachtingen

- Updates plannen en documenteren.
- SSH hardenen waar gebruikt.
- Least privilege toepassen.
- Proxmox user management gebruiken.
- Bitwarden of goedgekeurd alternatief gebruiken.
- bestaande VPN-toegang en routes op least privilege controleren.
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
- [ ] Onboarded service heeft passende authenticatie.
- [ ] Beheer- en automatiseringsinterfaces zijn niet onbeveiligd publiek bereikbaar.
- [ ] VPN-toegang volgt de bestaande aanvraag- en intrekkingsprocedure.
- [ ] Secrets staan in Bitwarden.
- [ ] Backups en exports bevatten geen zichtbare secrets.

## Verboden

- `allow all` als blijvende firewallstrategie.
- Onnodige anonieme write-access op een onboarded service.
- Onbeveiligde publieke beheer- of automatiseringsinterfaces.
- Private keys of recovery codes in repo.
- Bypass van OPNsense.
