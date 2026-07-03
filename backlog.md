# Backlog

Gebruik deze backlog als startpunt. Maak per groep concrete issues aan en wijs eigenaars toe.

## Must

- Groepsrepo clonen/forken en invullen.
- Toegang tot OPNsense en drie Proxmox-nodes controleren.
- Netwerkplan en IP-plan documenteren.
- Bewijzen dat alle nodes achter OPNsense zitten.
- Proxmox-cluster vormen.
- Proxmox SDN-zone en VNet maken.
- Proxmox users, rollen, pools en ACL's configureren.
- Beperkte account testen.
- Bitwarden of goedgekeurd alternatief gebruiken.
- Webshare veilig publiceren via OPNsense.
- VPN-toegang opzetten.
- Proxmox firewall met security groups gebruiken.
- n8n-workflow bouwen en testen.
- HA-testresource configureren en testen.
- Backup/restore-test uitvoeren.
- Monitoring en logging voorzien.
- Minstens een incident of change request volledig opvolgen.
- Einddemo voorbereiden.

## Should

- Interne DNS of duidelijke naamgeving voorzien.
- Dashboard voor interne services voorzien.
- Automatische healthcheck voor webshare of n8n maken.
- Firewallregels periodiek reviewen.
- Configuratievoorbeelden zonder secrets bewaren.
- Diagrammen up-to-date houden.

## Could

- Lichte reverse proxy gebruiken.
- Ansible of scripts voor beperkte automatisatie gebruiken.
- Extra testclient voorzien.
- Extra service toevoegen als resources dat toelaten.

## Vermijd

- Volledige Kubernetes-clusters.
- Zware Nextcloud-installaties zonder resourcebewijs.
- Meerdere Windows Servers.
- Grote databases.
- Uitgebreide SIEM-stacks.
- Alles tegelijk draaien zonder resourceplanning.

