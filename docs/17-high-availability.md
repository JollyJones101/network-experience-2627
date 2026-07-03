# High Availability

Jullie configureren Proxmox HA binnen de beperkingen van de nested labo-omgeving.

## Belangrijke nuance

Dit is geen volwaardige productie-HA-omgeving. Correct uitleggen waarom iets beperkt werkt is beter dan fout beweren dat het productiegeschikt is.

## Verwachtingen

- HA configureren;
- een kleine test-VM of test-container kiezen;
- storagekeuze documenteren;
- HA group en resource documenteren;
- gecontroleerd scenario testen;
- beperkingen en risico's benoemen.

## Mogelijke tests

- node maintenance;
- VM/container migratie;
- stop/start via HA;
- gesimuleerde node-uitval alleen als veilig toegestaan.

Gebruik [templates/ha-test-template.md](templates/ha-test-template.md).

