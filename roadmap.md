# Roadmap

Deze roadmap geeft een realistische 12-wekenplanning. De docent kan accenten, deadlines of volgorde aanpassen. Gebruik issues om taken per week te verdelen.

| Week | Thema | Deliverables |
|---:|---|---|
| 1 | Orientatie en toegang | Groepsrepo, rollen, toegangstest, Bitwarden-vault of alternatief, eerste netwerkplan |
| 2 | Basisnetwerk en OPNsense | LAN/WAN-controle, IP-plan, basisfirewall, NAT, bewijs dat alles achter OPNsense zit |
| 3 | Proxmox-cluster | Cluster met drie nodes, node naming, storagekeuze, test-VM of container |
| 4 | Proxmox SDN | SDN-zone, VNet, testconnectiviteit, netwerkdocumentatie |
| 5 | User management | Gebruikers, rollen, pools, ACL's, beperkte VM-beheeraccount, testbewijs |
| 6 | Webshare en Minecraft-basis | Filesharing-service, authenticatie, OPNsense-publicatie, firewall/NAT/reverse proxy, backupafspraak; Minecraft-architectuur, rollen en beveiligde basisserver |
| 7 | VPN | WireGuard of OpenVPN, peers/users, routes, firewallregels, testbewijs |
| 8 | Proxmox firewall | Firewall inschakelen, security groups, IP sets, toegelaten en geblokkeerd verkeer testen |
| 9 | n8n-automatisatie | Lichte n8n-installatie, beheerworkflow, credentials veilig beheren, workflowtest |
| 10 | High Availability | HA-configuratie, kleine testresource, migratie/failover-test, beperkingen documenteren |
| 11 | Monitoring, backup en incident | Monitoring/logging, restore-test, incidentrapport, verbeteracties; Minecraft-hub, BlueMap, performantiemeting en overdrachtsgids |
| 12 | Stabilisatie en eindoplevering | Documentatie finaliseren, demo, eindpresentatie, individuele technische bevraging |

## Iteratiedoelen

### Iteration 1 - Orientatie en basisconnectiviteit

- omgeving verkennen;
- toegang controleren;
- netwerkplan opstellen;
- OPNsense basisconfig controleren;
- Proxmox-nodes bereikbaar maken;
- eerste documentatie en issues aanmaken.

### Iteration 2 - Cluster en basisservices

- Proxmox-cluster vormen;
- storagekeuze documenteren;
- test-VM/container;
- Proxmox SDN opstarten;
- DNS/DHCP/firewallregels;
- eerste interne service.

### Iteration 3 - Security, backup en monitoring

- user management en least privilege;
- password management;
- VPN;
- Proxmox firewall/security groups;
- back-upstrategie en restore-test;
- monitoring en logging.

### Iteration 4 - Stabilisatie, incidenten en eindoplevering

- n8n-workflow afwerken;
- HA-test uitvoeren;
- incident of change request correct opvolgen;
- documentatie finaliseren;
- demo en reflectie voorbereiden.
