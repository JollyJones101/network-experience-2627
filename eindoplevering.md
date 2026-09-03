# Eindoplevering

De eindoplevering toont dat jullie omgeving technisch werkt, veilig beheerd wordt en professioneel gedocumenteerd is.

## Minimale demo

Elke groep demonstreert minstens:

1. toegang via VPN;
2. OPNsense als verplichte gateway;
3. Proxmox-cluster met drie nodes;
4. Proxmox SDN met minstens een werkend VNet;
5. beperkte Proxmox-account die alleen eigen VM's/containers kan beheren;
6. Bitwarden/password management-afspraken zonder secrets in GitHub;
7. webshare bereikbaar via WAN-kant, klaslokaalnetwerk of opleidingsnetwerk;
8. n8n-workflow die aantoonbaar werkt;
9. Proxmox firewall met security groups;
10. HA-configuratie met testresource;
11. back-up/restore-test;
12. technische documentatie en changelog;
13. incident of change request met correcte opvolging.
14. Minecraft-server: veilige spelersconnectie, beschermde hub, BlueMap volgens het gekozen publicatiemodel, rollenbewijs en restore-test.

## Documenten die klaar moeten zijn

- [groepsindeling.md](groepsindeling.md)
- [docs/05-netwerkplan.md](docs/05-netwerkplan.md)
- [docs/11-proxmox-sdn.md](docs/11-proxmox-sdn.md)
- [docs/12-proxmox-user-management.md](docs/12-proxmox-user-management.md)
- [docs/13-password-management.md](docs/13-password-management.md)
- [docs/14-webshare.md](docs/14-webshare.md)
- [docs/15-n8n-automatisatie.md](docs/15-n8n-automatisatie.md)
- [docs/16-proxmox-firewall-security-groups.md](docs/16-proxmox-firewall-security-groups.md)
- [docs/17-high-availability.md](docs/17-high-availability.md)
- [docs/18-vpn.md](docs/18-vpn.md)
- [docs/19-minecraft-server.md](docs/19-minecraft-server.md)
- [changelog.md](changelog.md)

## Presentatie

Gebruik een korte, technische structuur:

1. architectuur;
2. belangrijkste ontwerpkeuzes;
3. security en toegangsbeheer;
4. demo van kernonderdelen;
5. incident/change en wat jullie leerden;
6. beperkingen en verbeterpunten.

Iedere student moet technische vragen over de eigen bijdrage kunnen beantwoorden.
