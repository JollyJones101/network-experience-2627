# VM-template

## Identiteit

| Veld | Waarde |
|---|---|
| VMID en naam | `<ID_NAAM>` |
| Proxmox-pool | `<POOL>` |
| Omgeving/functie | `<PROD_TEST_FUNCTIE>` |
| Primaire/back-upeigenaar | `<ROLLEN>` |
| Aanmaak- en verwijderdatum | `<DATUM_BESLUIT>` |

## Resources

| vCPU | RAM | Disk | OS/image | Verwachte piek |
|---:|---:|---:|---|---|
| `<N>` | `<GB>` | `<GB>` | `<VERSIE_BRON>` | `<METING>` |

## Netwerk

| Interface | Zone/VLAN | IP/DNS | Gateway | Firewallprofiel |
|---|---|---|---|---|
| `<IFACE>` | `<ZONE>` | `<WAARDE>` | `<IP>` | `<PROFIEL>` |

## Lifecycle

- Deployment: `<SCRIPT_PLAYBOOK_OF_STAPPEN>`
- Patchvenster: `<AFSPRAAK>`
- Back-upklasse: `<KLASSE_OF_GEEN_MET_REDEN>`
- Monitoring: `<CHECKS_EN_ALERTS>`
- Secrets: `<VAULTREFERENTIE>`
- Stop/cleanup: `<PROCEDURE>`

## Validatie

- [ ] Baseline hardening en updates uitgevoerd.
- [ ] Alleen noodzakelijke services luisteren.
- [ ] Positieve en negatieve netwerktest uitgevoerd.
- [ ] Resourcegebruik gemeten.
- [ ] Monitoring en back-up getest.
- [ ] Rebuild- of herstelpad is gedocumenteerd.
