# Monitoring, logging en servicelevels

Observeer wat gebruikers en beheerders nodig hebben. Elk signaal heeft een doel, eigenaar en reactie.

## Vier lagen

1. **Gebruikerservaring:** kan de belangrijkste flow worden uitgevoerd?
2. **Applicatie:** fouten, wachtrij, tick rate, ingestie of jobspecifieke metrics.
3. **Systeem:** CPU, RAM, disk, I/O, processen en tijd.
4. **Afhankelijkheden:** DNS, certificaat, database, externe API en back-up.

## Minimale alertmatrix

| Signaal | Drempel/conditie | Ernst | Eigenaar | Actie/runbook |
|---|---|---|---|---|
| Dienst onbereikbaar | `<N_METINGEN>` | hoog | `<ROL>` | `<LINK>` |
| Capaciteit | `<GRENS_EN_DUUR>` | middel | `<ROL>` | `<LINK>` |
| Projectspecifiek | `<SLO>` | `<ERNST>` | `<ROL>` | `<LINK>` |
| Back-up/check faalt | `<CONDITIE>` | hoog | `<ROL>` | `<LINK>` |

Test alerts gecontroleerd. Een alert die niemand ontvangt of waarvoor geen actie bestaat, is geen bruikbare alert.

## Logging en privacy

- Log beveiligings- en beheeracties die nodig zijn voor diagnose.
- Masker secrets en minimaliseer persoonsgegevens.
- Stel rotatie en retentie in om diskuitputting te voorkomen.
- Beperk toegang; logs zijn geen publieke dataset.
- Synchroniseer tijd zodat events correleerbaar zijn.
- Documenteer wat bewust niet wordt gelogd.

## Servicelevels

Formuleer twee of drie meetbare SLI's, bijvoorbeeld beschikbaarheid, responstijd, job-successratio, TPS, ingestielatency of hersteltijd. Kies realistische SLO's voor de onderwijscontext en rapporteer het resultaat eerlijk.
