# Back-up, restore en continuïteit

Een Proxmox-back-up alleen is geen herstelstrategie. De groep bepaalt welke data uniek is, hoe consistent ze wordt opgeslagen en hoe de dienst opnieuw bruikbaar wordt.

## Classificeer eerst

| Type | Voorbeelden | Aanpak |
|---|---|---|
| Reproduceerbaar | OS, packages, containerimages | deploymentcode en versiepinning |
| Configuratie | serviceconfig, workflowexports | Git zonder secrets plus veilige secretprocedure |
| Unieke data | werelden, database, gebruikersinhoud | goedgekeurde back-up met retentie |
| Tijdelijk | caches, CI-artifacts, testdata | meestal uitsluiten en automatisch opschonen |

## Leg per dienst vast

- recovery point objective: hoeveel data mag maximaal verloren gaan?
- recovery time objective: hoe snel moet de dienst terug zijn?
- back-upmethode, planning, retentie en encryptie;
- eigenaar en controle op mislukte jobs;
- afhankelijkheden en volgorde van herstel;
- locatie van secrets en sleutels;
- verwijdering bij einde project.

## Verplichte restoretest

Herstel nooit over de enige productie-instantie. Gebruik een aparte VM, database of namespace, valideer functionele data en ruim de test gecontroleerd op. Noteer gemeten duur, dataverlies, problemen en verbeteracties in [backup-test-template.md](templates/backup-test-template.md).

Een snapshot vóór een update is nuttig voor korte rollback, maar geen vervanging voor een onafhankelijke back-up.
