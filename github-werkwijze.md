# GitHub-werkwijze

## Groepsrepo

Elke groep werkt in een eigen clone of fork van deze blueprint. Gebruik niet de centrale blueprint als gedeelde werkrepo voor alle groepen.

## Issues

Gebruik issues voor:

- projecttaken;
- supportvragen;
- incidenten;
- change requests;
- technische vragen;
- documentatieproblemen.

Een issue mag pas dicht wanneer:

- de taak uitgevoerd is;
- validatie of testbewijs toegevoegd is;
- relevante documentatie bijgewerkt is;
- risico's of rollback genoteerd zijn waar nodig.

## Labels

Gebruik labels zoals:

- `feature`
- `fix`
- `chore`
- `docs`
- `support`
- `incident`
- `change`
- `question`
- `must`
- `should`
- `could`

## Commits

Schrijf commits kort en duidelijk:

```text
docs: voeg netwerkplan voor groep 4 toe
fix: corrigeer firewallregel voor webshare
change: documenteer VPN peer intrekking
```

## Pull requests

Gebruik pull requests voor grotere wijzigingen of review door groepsleden. Een PR bevat:

- samenvatting;
- gekoppelde issue(s);
- testbewijs;
- documentatie-impact;
- bevestiging dat er geen secrets in staan.

## Bestandsafspraken

- Documentatie: Markdown in `docs/` of rootbestanden.
- Screenshots: `images/`.
- Diagrammen: `diagrams/`.
- Configuratievoorbeelden: `configs/`, altijd zonder secrets.
- Scripts: `scripts/`, met duidelijke uitleg en veilige defaults.

## Changelog

[changelog.md](changelog.md) bevat belangrijke wijzigingen. De GitHub Action vult bij gesloten issues automatisch een entry aan. Manuele aanvullingen mogen ook.

