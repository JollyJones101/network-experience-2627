# Proxmox user management

Iedereen permanent als `root` laten werken is geen professioneel beheer. Jullie richten een rollen- en rechtenmodel in.

## Minimale realisatie

- minstens een groepsbeheeraccount;
- minstens een beperkte account;
- Proxmox-pool voor afgebakende resources;
- rollen en ACL's;
- testbewijs dat de beperkte account wel eigen VM's/containers kan beheren, maar geen clusterinstellingen of resources buiten scope.

## Te documenteren

Gebruik [templates/user-management-template.md](templates/user-management-template.md).

- gebruikers;
- rollen;
- pools;
- ACL-paden;
- toegekende rechten;
- testresultaten;
- screenshots zonder secrets.

## Verplichte tests

- beperkte account maakt een eigen VM/container aan;
- beperkte account start/stopt eigen resource;
- beperkte account verwijdert eigen resource;
- beperkte account kan geen andere VM's beheren;
- beperkte account kan geen clusterinstellingen aanpassen.

