# Accounts- en rollenmatrix

## Rollen

| Rol | Toegestane acties | Verboden acties | Goedkeurder |
|---|---|---|---|
| `<ROL>` | `<ACTIES>` | `<ACTIES>` | `<ROL>` |

## Accounts en lifecycle

| Account/serviceaccount | Rol | Eigenaar | MFA/key | Aanmaak | Review/verval | Secretlocatie |
|---|---|---|---|---|---|---|
| `<ACCOUNT>` | `<ROL>` | `<NAAM>` | `<METHODE>` | `<DATUM>` | `<DATUM>` | `<VAULTREF_OF_NVT>` |

## Proxmox-scope

| Subject | Pad/pool | Rol | Reden |
|---|---|---|---|
| `<GROEP_OF_USER>` | `<POOL>` | `<ROL>` | `<REDEN>` |

## Rechtentests

- [ ] Gewone gebruiker kan de bedoelde gebruikersflow.
- [ ] Gewone gebruiker kan geen moderator-/adminactie.
- [ ] Operator kan beheren maar geen OS- of platformadminactie.
- [ ] Serviceaccount kan alleen de noodzakelijke machineactie.
- [ ] Groepslid kan eigen VM's maar geen andere pool beheren.
- [ ] Ingetrokken account of credential werkt niet meer.

## Onboarding, review en offboarding

`<STAPPEN_MET_EIGENAAR_EN_BEWIJS>`
