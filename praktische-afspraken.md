# Praktische afspraken

## Werkwijze

Elke groep gebruikt een eigen clone of fork van deze blueprint. De repo is tegelijk projectdossier, technische documentatie en overdrachtspakket. Werk vanaf de eerste week met issues en pull requests; achteraf samengestelde documentatie is zelden betrouwbaar.

## Gedeelde productieomgeving

Smith is geen persoonlijke homelabserver. Houd rekening met andere groepen en bestaande diensten:

- blijf binnen de toegewezen pool, VMID-range, netwerken en resourcequota;
- maak geen privileged containers tenzij de docent dit uitdrukkelijk goedkeurt;
- plan belastende tests en onderhoud met de docent;
- zet ongebruikte test-VM's uit en verwijder ze na goedkeuring;
- meld onverwachte belasting, kwetsbaarheden en incidenten onmiddellijk;
- voer geen scans uit buiten de expliciet toegewezen projectscope.

## Groepswerking

- Wijs een primaire en secundaire eigenaar toe voor elk kritisch onderdeel.
- Laat minstens twee groepsleden elke kernservice kunnen beheren en herstellen.
- Houd wekelijks een kort statusmoment bij met beslissingen, bewijs en blokkades.
- Gebruik issues met een eigenaar, deadline en acceptatiecriteria.
- Laat betekenisvolle wijzigingen reviewen via een pull request.
- Noteer externe afspraken en toestemmingen in de repo, zonder persoonsgegevens die er niet thuishoren.

## Rol van de docent

De docent beheert Smith en de gedeelde infrastructuur, keurt risicovolle changes goed, bewaakt capaciteit en veiligheid en helpt bij goed omschreven blokkades. De groep blijft eigenaar van analyse, implementatie, testen, documentatie en eerstelijnsdiagnose van het eigen project.

## Productiechanges

Een wijziging met impact op andere gebruikers, publieke bereikbaarheid, gedeelde infrastructuur of een evenement vereist vooraf een change request. Zie [change-management.md](change-management.md).

## Externe communicatie

Communicatie naar alle studenten, personeel, Stuvo of externe deelnemers wordt eerst door de docent of aangeduide verantwoordelijke goedgekeurd. Gebruik geen echte mailinglijsten of persoonsgegevens voor tests.

## Deadlines en aanwezigheid

Exacte deadlines worden door de docent bevestigd. De [roadmap](roadmap.md) bevat de standaardplanning. Aanwezigheid tijdens contactmomenten en aantoonbare wekelijkse voortgang worden verwacht.
