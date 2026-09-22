# Security, privacy en hardening

## Baseline voor elke VM

- ondersteund OS en alleen noodzakelijke packages;
- automatische of geplande security-updates met eigenaar;
- persoonlijke SSH-sleutels, geen gedeeld rootwachtwoord;
- sudo en serviceaccounts volgens least privilege;
- hostfirewall met expliciet noodzakelijke poorten;
- diensten luisteren alleen op bedoelde interfaces;
- tijdsynchronisatie, logrotatie en diskmonitoring;
- secrets buiten Git, images en shell history;
- periodieke controle op ongebruikte accounts en services.

## Applicatie

- rollenmatrix en negatieve rechtentests;
- MFA voor beheer waar beschikbaar;
- veilige sessies, TLS en correcte proxy-instellingen;
- inputvalidatie, rate limiting en beperkte foutdetails;
- dependency- en imageupdates;
- veilige credentialrotatie en intrekking;
- dataminimalisatie, bewaartermijn en cleanup.

## Threat model

Beschrijf minstens:

1. waardevolle assets en gevoelige data;
2. trustgrenzen en toegangspaden;
3. vijf relevante dreigingen;
4. preventie, detectie en herstel;
5. resterend risico en eigenaar.

Test alleen binnen de eigen projectscope. Een portscan of securitytest tegen Smith, campusdiensten of andere groepen is nooit impliciet toegestaan.

## Pre-productiecheck

- [ ] Beheerinterface niet publiek bereikbaar.
- [ ] Standaardaccounts en -wachtwoorden verwijderd.
- [ ] Rollen en geblokkeerde acties getest.
- [ ] Netwerkregels minimaal en gedocumenteerd.
- [ ] Secretscan op repo en artifacts uitgevoerd.
- [ ] Back-updata en logs op gevoelige inhoud gecontroleerd.
- [ ] Alerts voor mislukte login of relevante misbruikspatronen ingesteld.
- [ ] Stop-, revoke- en incidentprocedure gekend.
