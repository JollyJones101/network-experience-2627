# Proxmox-cluster

Jullie bouwen een Proxmox-cluster met drie virtuele nodes:

- pve-x-01;
- pve-x-02;
- pve-x-03.

Dit is een nested labo-omgeving, geen productiecluster met volledige performance. Documenteer beperkingen eerlijk.

## Verwachtingen

- Controleer bereikbaarheid van alle nodes.
- Vorm een cluster.
- Gebruik consequente node naming.
- Documenteer storagekeuzes.
- Maak minstens een test-VM of test-container.
- Richt users, rollen, pools en ACL's in.
- Gebruik Proxmox SDN.
- Gebruik Proxmox firewall en security groups.
- Configureer HA met een kleine testresource.
- Documenteer beperkingen van nested virtualization.

## Storage

Beschrijf:

- welke storage beschikbaar is;
- waarvoor ze gebruikt wordt;
- of migratie of HA realistisch mogelijk is;
- welke risico's er zijn;
- hoe back-ups gemaakt worden.

## VM/CT-netwerken

Documenteer per VM/container:

- naam;
- hostnode;
- netwerk;
- IP-adres;
- firewallprofiel;
- doel;
- eigenaar.

Gebruik [templates/server-template.md](templates/server-template.md) of [templates/service-template.md](templates/service-template.md).

