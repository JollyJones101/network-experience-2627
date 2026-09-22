# Service-template

## Identiteit

| Veld | Waarde |
|---|---|
| Service en versie | `<NAAM_VERSIE>` |
| Doel en gebruikers | `<DOELGROEP>` |
| Eigenaar/back-up | `<ROLLEN>` |
| VM(s) | `<VMID_NAMEN>` |
| Kriticiteit | `<LAAG_MIDDEL_HOOG>` |

## Architectuur

`<LINK_NAAR_DIAGRAM_EN_DATAFLOW>`

## Deployment en configuratie

- Bron/image: `<BETROUWBARE_BRON>`
- Deployment: `<LINK_NAAR_AUTOMATISERING>`
- Configuratie: `<LINK_ZONDER_SECRETS>`
- Secrets: `<VAULTREFERENTIE>`
- Update/rollback: `<RUNBOOK>`

## Netwerk en toegang

| Bron/rol | Bestemming | Poort | Toegang | Reden |
|---|---|---:|---|---|
| `<BRON>` | `<DOEL>` | `<POORT>` | `<ALLOW_DENY>` | `<REDEN>` |

## Operations

- SLI/SLO: `<METING_EN_DOEL>`
- Monitoring/alerts: `<LINK>`
- Logs/retentie: `<AFSPRAAK>`
- Back-up/RPO/RTO: `<AFSPRAAK>`
- Restoretest: `<LINK>`
- Incidentrunbook: `<LINK>`

## Acceptatie

- [ ] Belangrijkste gebruikersflow werkt.
- [ ] Rollen en ongewenste toegang zijn getest.
- [ ] Failure- en herstelpad zijn getest.
- [ ] Resources blijven binnen budget.
- [ ] Beheerder buiten het bouwteam kan het runbook volgen.
