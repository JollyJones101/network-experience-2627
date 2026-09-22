# Documentatiestandaard

Schrijf voor een opvolger die het project niet heeft gebouwd. Documentatie beschrijft zowel normale werking als falen.

## Technisch ontwerp

```text
# Titel en eigenaar
## Doel en gebruikers
## Context en afhankelijkheden
## Architectuur, netwerk en dataflow
## Beslissingen en alternatieven
## Resources en capaciteit
## Security en privacy
## Deployment en configuratie
## Monitoring en servicelevels
## Back-up, restore en rollback
## Tests en bewijs
## Gekende beperkingen
## Metadata: datum, auteur, reviewers, issues
```

## Runbook

Een runbook bevat:

- trigger of symptoom;
- voorwaarden en vereiste toegang;
- veilige, genummerde stappen;
- verwachte output en beslismomenten;
- escalatie en stopconditie;
- validatie en terugkeer naar normale toestand;
- cleanup en registratie achteraf.

Maak minstens runbooks voor deployment/update, dagelijks beheer, veelvoorkomende storing, credentialrotatie, back-up/restore en gecontroleerd uitschakelen.

## Beslissingslog

Leg belangrijke technische keuzes kort vast met context, opties, beslissing, argumenten, gevolgen en datum. Vermijd documenten die alleen beschrijven wat werd geïnstalleerd.

## Regels

- Schrijf reproduceerbaar en test commando's.
- Gebruik placeholders voor secrets en gevoelige waarden.
- Link naar issues, pull requests en changelog.
- Bewijs met tekst/export waar dat beter leesbaar is dan screenshots.
- Noteer relevante mislukte hypotheses en wat ervan geleerd is.
- Werk documenten bij in dezelfde wijziging als de configuratie.
