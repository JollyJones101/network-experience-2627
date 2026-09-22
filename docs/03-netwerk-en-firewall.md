# Netwerk, firewall en publicatie

## Uitgangspunt

De opleiding bepaalt welke bridge, VLAN, subnetten, gateways en gedeelde netwerkdiensten beschikbaar zijn. Studenten ontwerpen het netwerkpad van hun workloads, maar wijzigen geen switching, routing of perimeter zonder goedgekeurde change.

## Zones

Beschrijf voor elk project minstens:

- **beheer:** alleen voor beheerders via het afgesproken pad;
- **applicatie:** verkeer tussen gebruikers en dienst;
- **data:** database, broker of opslag, niet rechtstreeks voor eindgebruikers;
- **monitoring/back-up:** alleen de noodzakelijke bronnen en bestemmingen;
- **test/staging:** logisch gescheiden van productie waar relevant.

Niet elk project krijgt afzonderlijke VLANs. Gebruik dan hostfirewalls, servicebinding, authenticatie en afzonderlijke accounts om dezelfde trustgrenzen zo goed mogelijk af te dwingen.

## Publicatie

Een interne of publieke dienst vraagt een gedocumenteerd pad:

```text
client → goedgekeurde DNS/reverse proxy/firewall → applicatie-VM → datadienst
```

Leg bron, bestemming, protocol, poort, TLS, authenticatie, logging en eigenaar vast. Beheerpoorten, databases, RCON, MQTT-beheer en dashboards worden niet rechtstreeks publiek gemaakt.

## Firewalltests

Test minimaal:

- toegelaten gebruiker naar bedoelde service;
- niet-toegelaten bron naar service;
- applicatie naar noodzakelijke datadienst;
- gebruiker rechtstreeks naar datadienst;
- beheer vanaf toegestaan en niet-toegestaan pad;
- uitgaand verkeer dat wel en niet nodig is.

Gebruik [firewall-rule-template.md](templates/firewall-rule-template.md) en registreer gedeelde wijzigingen als change request.
