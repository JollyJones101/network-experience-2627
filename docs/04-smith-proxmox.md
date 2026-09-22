# Werken op Proxmox-node Smith

## Wat jullie beheren

Binnen de eigen pool mogen studenten volgens de toegewezen rol VM's maken en hun lifecycle beheren. De groep is verantwoordelijk voor naamgeving, inventaris, gast-OS, applicaties, updates, resources en cleanup.

## Naamgeving

Gebruik de door de docent bevestigde conventie, bijvoorbeeld:

```text
nx-g<groep>-<omgeving>-<functie>-<nummer>
nx-g03-prod-app-01
nx-g03-test-db-01
```

Gebruik alleen VMID's uit de toegewezen range.

## VM of container

Gebruik standaard een VM. Een LXC-container is alleen geschikt als de opleiding dit toestaat en de groep de security- en back-upimplicaties kan uitleggen. Privileged containers zijn niet toegestaan zonder expliciete uitzondering.

## Resourcebeheer

- Reserveer niet automatisch het groepsmaximum.
- Start klein en schaal op basis van metingen.
- Gebruik geen memory ballooning of CPU overcommit als aanname zonder bevestiging.
- Houd voldoende headroom voor piek, update en restore.
- Stel meldingen in voor diskgroei en langdurig hoge belasting.
- Documenteer tijdelijke loadtests en stopcondities.

Gebruik het [resourcebudget-template](templates/resourcebudget-template.md).

## Lifecycle

Elke VM heeft een eigenaar, functie, omgeving, resourceprofiel, netwerkpad, back-upklasse, patchvenster en verwijderbesluit. Templates, cloud-init of configuration management hebben de voorkeur boven handmatige snowflake-servers.

## Verboden beheeracties

Studenten wijzigen geen nodepackages, Proxmox repositories, storage, bridges, clusterconfiguratie, hostfirewall of andere pools. Vraag dit via een change request wanneer het project een legitieme afhankelijkheid heeft.
