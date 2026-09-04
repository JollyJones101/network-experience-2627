# Proxmox-cluster

Jullie krijgen een werkend Proxmox-cluster met drie virtuele nodes:

- pve-x-01;
- pve-x-02;
- pve-x-03.

Dit is een nested labo-omgeving, geen productiecluster met volledige performance. Documenteer beperkingen eerlijk.

## Geen installatieopdracht

Het vormen van het cluster, de basisbekabeling en de initiële storageconfiguratie zijn al uitgevoerd. Deze opnieuw uitvoeren levert geen punten op. Behandel het cluster als een overgenomen platform en wijzig gedeelde basisinstellingen alleen via een goedgekeurde change.

## Beschikbare mogelijkheden

Binnen de toegewezen rechten ondersteunt het platform VM's, containers, pools, ACL's, Proxmox SDN, firewallregels en beperkte HA-tests. De beschikbare capaciteit en beperkingen van nested virtualization worden door de docent meegedeeld.

## Storage

Relevante aandachtspunten zijn:

- welke storage beschikbaar is;
- waarvoor ze gebruikt wordt;
- of migratie of HA realistisch mogelijk is;
- welke risico's er zijn;
- hoe back-ups gemaakt worden.

## VM/CT-netwerken

Gebruik voor de inventarisatie per VM/container:

- naam;
- hostnode;
- netwerk;
- IP-adres;
- firewallprofiel;
- doel;
- eigenaar.

Gebruik [templates/server-template.md](templates/server-template.md) of [templates/service-template.md](templates/service-template.md).
