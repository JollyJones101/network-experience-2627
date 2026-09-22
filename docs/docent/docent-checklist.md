# Docent-checklist

## Intake Smith

- [ ] Persoonlijke accounts werken en MFA/SSH-afspraken zijn duidelijk.
- [ ] Groep ziet en beheert alleen de eigen pool.
- [ ] VMID-range, VLAN/subnet en naamconventie zijn meegedeeld.
- [ ] vCPU-, RAM- en diskbudget zijn vastgelegd.
- [ ] Procedure voor DNS, publicatie, firewall en back-up is duidelijk.
- [ ] Noodstop en escalatiepad zijn gekend.

## Gate 1 — charter

- [ ] Projectfiche, doelgroep en opdrachtgever zijn bevestigd.
- [ ] Must / Should / Could / Won't is haalbaar.
- [ ] Rollen, stakeholders en succesmetingen zijn ingevuld.
- [ ] Grootste risico's en externe afhankelijkheden zijn zichtbaar.

## Gate 2 — architectuur

- [ ] Architectuur-, netwerk- en dataflowdiagram zijn coherent.
- [ ] Resourcebudget bevat piek, groei en headroom.
- [ ] Trustgrenzen, rollen en dataclassificatie zijn beschreven.
- [ ] Proof-of-concept beantwoordt de grootste onzekerheid.
- [ ] Gedeelde changes zijn aangevraagd, niet stilzwijgend aangenomen.

## Gate 3 — productie-intake

- [ ] Deployment is reproduceerbaar.
- [ ] Hardening, patching en secretbeheer voldoen.
- [ ] Positieve en negatieve toegangsproeven slagen.
- [ ] Monitoring, logs en bruikbare alerts zijn aanwezig.
- [ ] Back-up bestaat en restore is gepland.
- [ ] Beheer- en incidentrunbooks zijn bruikbaar.

## Eindcontrole

- [ ] Projectspecifieke Must-acceptatietests slagen.
- [ ] Echte gebruikerstest of goedgekeurde dry-run is uitgevoerd.
- [ ] Restore/rollback is aantoonbaar getest.
- [ ] Resourcegebruik blijft binnen budget.
- [ ] Issues, reviews en commits tonen individuele bijdragen.
- [ ] Open risico's, tijdelijke accounts en cleanup zijn afgehandeld.
- [ ] Een volgende beheerder kan de dienst overnemen of gecontroleerd uitschakelen.
