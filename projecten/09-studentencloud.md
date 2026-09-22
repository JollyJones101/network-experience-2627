# Project 9 — Studentencloud voor bestanden

## Opdracht

Bouw een veilige interne filesharingdienst waarmee studenten en projectgroepen bestanden kunnen opslaan, synchroniseren en gecontroleerd delen. De oplossing moet gebruiksvriendelijk zijn, maar tegelijk quota, rollen, lifecycle, privacy, malware-risico, back-up en herstel professioneel behandelen.

Het project is geen poging om commerciële cloudopslag volledig na te bouwen. De groep kiest een haalbare doelgroep en bewijst dat de afgesproken kern betrouwbaar beheerd kan worden.

## Gebruikers en stakeholders

- individuele studenten;
- projectgroepen met gedeelde mappen;
- docenten of begeleiders die bestanden ontvangen of delen;
- servicebeheerders en privacyverantwoordelijke.

Interview gebruikers over bestandsgrootte, samenwerking, externe links, versieherstel en verwachtingen bij verwijdering.

## Must

- Een ondersteund open-source filesharingplatform met gemotiveerde toolkeuze.
- Authenticatie met persoonlijke accounts; MFA voor beheerders waar beschikbaar.
- Rollen voor gebruiker, groepsbeheerder, supportoperator en platformbeheerder.
- Persoonlijke opslag en groepsmappen met aantoonbare scheiding.
- Quota per gebruiker en/of groep, plus waarschuwing bij bijna volle opslag.
- Gecontroleerde deelmogelijkheden: intern delen en tijdelijke externe link met wachtwoord en vervaldatum.
- Externe publieke links standaard uit of strikt begrensd volgens de afgesproken scope.
- Versie- of prullenbakbeleid met duidelijke retentie.
- Veilige uploadlimieten en maatregelen tegen gevaarlijke bestanden, bijvoorbeeld blokkadebeleid of malwarecontrole.
- TLS via het goedgekeurde publicatiepad en geen publieke database- of beheerpoort.
- Monitoring van bereikbaarheid, opslaggroei, fouten, database, certificaat en back-up.
- Back-up van bestanden, metadata en configuratie met een geteste restore.
- Onboarding, offboarding, accountreview en verwijderprocedure.
- Gebruikersgids voor synchronisatie, delen, quota en herstel.

## Should

- Desktop- of mobiele synchronisatieproef met conflictafhandeling.
- File drop waarmee iemand bestanden kan aanleveren zonder bestaande inhoud te zien.
- Automatische waarschuwing voor verlopen accounts of links.
- Dashboard voor capaciteit en groeiprognose.
- SSO wanneer een geschikte gedeelde identiteitsdienst beschikbaar is.

## Could

- Integratie met een documenteditor, alleen na resource- en securitymeting.
- Aanvragen van groepsmappen via het selfserviceportaal.
- Versleutelde projectspecifieke opslag met gedocumenteerd sleutelherstel.
- Gecontroleerde gastaccounts voor een beperkte pilot.

## Niet in scope

- onbeperkte gratis opslag of belofte van permanente bewaring;
- anonieme publieke uploads zonder rate-, quota- en malwaremaatregelen;
- opslag van bijzondere categorieën persoonsgegevens of officiële dossiers;
- server-side encryptie presenteren als bescherming tegen gecompromitteerde beheerders zonder correcte analyse;
- syncclients uitrollen op toestellen zonder toestemming;
- back-up verwarren met synchronisatie of prullenbak.

## Acceptatietests

| Scenario | Geslaagd wanneer |
|---|---|
| Persoonlijke opslag | gebruiker A kan eigen bestanden beheren maar niet die van gebruiker B bekijken |
| Groepsmap | leden krijgen afgesproken rechten; verwijderd lid verliest toegang |
| Quota | upload boven limiet wordt correct geweigerd zonder bestaande data te beschadigen |
| Externe link | wachtwoord en vervaldatum werken; verlopen link geeft geen toegang |
| Verdacht bestand | afgesproken blokkade- of scanproces treedt aantoonbaar in werking |
| Syncconflict | twee wijzigingen veroorzaken geen stil, onverklaard dataverlies |
| Account offboarding | toegang wordt ingetrokken en data volgt het vastgelegde overdrachts-/verwijderbeleid |
| Restore | geselecteerde bestanden én metadata/rechten worden naar een testlocatie hersteld |

## Mijlpalen

- Week 2: doelgroep, dataclassificatie, bewaarbeleid en succescriteria.
- Week 4: platformvergelijking, storage- en resourceproef.
- Week 6: interne alpha met persoonlijke en groepsopslag.
- Week 8: delen, quota, hardening, monitoring en back-up.
- Week 10: pilot met representatieve gebruikers en restore-oefening.
- Week 12: capaciteitsadvies, gebruikersdocumentatie en overdracht.

## Verplichte bewijsstukken

Toolvergelijking, dataflow- en storagediagram, rollenmatrix, privacy- en retentieanalyse, quotabeleid, malwaremaatregelen, capaciteitsmeting, toegangsproeven, sync- en linktests, restorebewijs en onboarding/offboardingrunbooks.
