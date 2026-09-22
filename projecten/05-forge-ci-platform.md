# Project 5 — Forge & Ship: ontwikkelplatform

## Opdracht

Bouw een compacte interne softwareforge waarmee studententeams code veilig kunnen beheren, testen, bouwen en als containerimage publiceren. Denk aan Forgejo/Gitea, gecontroleerde runners en een private registry. Het platform moet eenvoudig te gebruiken én beheersbaar zijn binnen het resourcebudget van Smith.

## Must

- Git-platform met organisaties/teams, MFA waar mogelijk, least privilege en beschermd beheeraccount.
- Private containerregistry met authenticatie, quota, garbage collection en TLS via het afgesproken pad.
- Eén geïsoleerde runner die geen toegang heeft tot de Proxmox-host en niet standaard privileged draait.
- Voorbeeldproject met lint/test, image build, vulnerability scan en publicatie met immutable versie-tag.
- Branch protection, pull-requestreview en afgeschermde CI-secrets.
- Onboarding en offboarding voor student, maintainer en platformbeheerder.
- Monitoring van beschikbaarheid, jobduur/falen, diskgebruik, registrygroei en certificaat.
- Back-up en restore van repositories, metadata en registryconfiguratie; duidelijk onderscheid met reproduceerbare images.
- Update- en incidentrunbook, inclusief gecompromitteerde token of runner.

## Should

- Deployment naar een aparte demo-VM met handmatige approval.
- Dependabot/Renovate-achtige dependencyvoorstellen zonder automatische productie-uitrol.
- Signed images of provenance-bewijs.
- Projecttemplates en een korte developer onboarding.

## Could

- SSO na goedkeuring.
- Tijdelijke runners met aantoonbare cleanup.
- Software bill of materials in de pipeline.

## Niet in scope

- Docker socket van Smith of brede hostmounts;
- willekeurige publieke registratie;
- latest als enige image-tag;
- secrets in pipelinebestanden of logs;
- automatisch uitvoeren van onbetrouwbare forkcode op een runner met interne toegang.

## Acceptatietests

| Scenario | Geslaagd wanneer |
|---|---|
| Nieuwe ontwikkelaar | krijgt projecttoegang zonder platformadmin te worden |
| Mergecontrole | ongeteste of niet-gereviewde wijziging kan de beschermde branch niet bereiken |
| Build | versieerbaar image wordt getest, gescand en gepubliceerd |
| Secret | CI-secret verschijnt niet in repository, artifact of log |
| Runneraanval | testjob kan geen Smith- of andere projectresources beheren |
| Registryquota | groei wordt begrensd en oude testimages worden beheerst opgeruimd |
| Restore | repository en platformmetadata zijn bruikbaar teruggezet |

## Mijlpalen en bewijs

- Week 2: gebruikersflows en supply-chain-dreigingen.
- Week 4: forge/registry/runnerarchitectuur.
- Week 6: eerste complete pipeline.
- Week 8: rollen, hardening, monitoring en back-up.
- Week 10: pilot met een ander studententeam.
- Week 12: platformcatalogus en overdracht.

Lever dataflowdiagram, permissionsmatrix, pipelineconfiguratie, runner threat model, image lifecycle, scanresultaten, restorebewijs en developer-/adminhandleiding op.
