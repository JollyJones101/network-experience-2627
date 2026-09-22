# Toegang, accounts en Proxmox-scope

## Persoonlijke toegang

Iedere student gebruikt een persoonlijk account. Accounts, MFA-codes en SSH-private keys worden nooit gedeeld. Gedeelde applicatiecredentials zijn uitzonderlijk en worden beheerd via de afgesproken vault.

| Systeem | Account/rol | Bereik | Eigenaar |
|---|---|---|---|
| Proxmox | `<PERSOONLIJK_ACCOUNT>` | `<EIGEN_POOL>` | opleiding |
| VM-beheer | `<SSH_ACCOUNT>` | eigen VM's | groep |
| Applicatie | `<ROL>` | volgens project | groep |
| Vault | `<GROEPSCOLLECTIE>` | projectsecrets | groep/opleiding |

## Proxmox-rechtentest

Voer samen met de docent een positieve en negatieve test uit:

- eigen bestaande VM bekijken, starten en stoppen;
- binnen quota een kleine test-VM aanmaken;
- eigen console openen;
- geen VM van een andere groep bekijken of wijzigen;
- geen node-, storage-, netwerk- of datacenterinstellingen wijzigen;
- geen VM buiten de eigen pool verplaatsen;
- test-VM na validatie gecontroleerd verwijderen.

Meld een te ruim recht onmiddellijk. Gebruik het niet om verder te verkennen.

## OS- en applicatieaccounts

- Beperk rechtstreeks rootgebruik en gebruik persoonlijke sudo-accounts.
- Gebruik servicespecifieke accounts zonder interactieve login.
- Leg rollen en intrekkingsprocedure vast.
- Verwijder testaccounts na acceptatie.
- Roteer credentials bij overdracht of vermoeden van lek.

## Noodtoegang

Documenteer wie bij verlies van toegang, incident of afwezigheid mag ingrijpen. Een break-glasscredential staat nooit in Git en het gebruik ervan wordt gelogd en achteraf geëvalueerd.
