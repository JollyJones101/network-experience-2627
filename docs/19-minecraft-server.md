# Minecraft-server voor de opleiding

## Opdracht

Richt en beheer samen een nette, veilige en duurzame Minecraft-omgeving voor de opleiding. De server is bedoeld als een blijvende ontmoetingsplaats voor studenten uit alle drie de jaren en voor docenten. Het is dus geen tijdelijke demo: ontwerp de omgeving zodat een volgende lichting ze veilig kan overnemen en verder uitbouwen.

De Minecraft-server is een verplichte, geïntegreerde service binnen de labo-omgeving. Kies een lichte, goed onderhouden serverimplementatie (bijvoorbeeld Paper) en documenteer de gekozen versie, licenties en compatibiliteit. Gebruik alleen plugins, mods en content waarvoor jullie de gebruiks- en distributievoorwaarden respecteren. Een modpack of zware modded-server kan alleen na voorafgaande toestemming van de docent en met aantoonbaar resourcebudget.

## Minimumresultaat

De groep levert minstens het volgende op:

- een stabiele Minecraft-server die na een herstart automatisch opstart;
- een duidelijke, veilige toegang voor spelers, zonder beheerinterfaces publiek open te zetten;
- een verzorgde hub/spawn met welkomstinformatie, regels, wegwijzers en een veilige spelerszone;
- een aparte beheerzone of testwereld die gewone spelers niet kunnen wijzigen;
- een online kaart met BlueMap of een gelijkwaardig, vooraf goedgekeurd alternatief;
- onderbouwde optimalisaties voor serverprestaties en wereldgrootte;
- een beargumenteerde rol- en rechtenstructuur voor spelers, moderators, beheerders en docenten;
- backup, restore-test, monitoring, logging en een overdrachtsplan voor volgende cohorten.

## Architectuur en netwerk

- Plaats de server in een afzonderlijk server- of game-VNet achter OPNsense. Maak de noodzakelijke firewallregels expliciet en hanteer deny-by-default.
- Publiceer alleen de strikt nodige spelpoort. Houd Proxmox, SSH, RCON, BlueMap-beheer en plugins met een beheerinterface intern of uitsluitend via VPN bereikbaar.
- Gebruik een DNS-naam indien beschikbaar; documenteer de DNS-, NAT- en firewallketen.
- Documenteer host, VM/LXC/Docker-keuze, toegewezen CPU/RAM/storage en het verwachte aantal gelijktijdige spelers. Kies licht en reserveer capaciteit voor de verplichte kernservices.
- Spreek met de docent af of de spelpoort vanaf het internet, enkel via campusnetwerk of enkel via VPN toegankelijk is. Gebruik nooit een omweg rond OPNsense.

## Wereld, hub en spelerservaring

- Voorzie minstens een hub/spawn die duidelijk afgewerkt is: welkomstbord of -tekst, gedragsregels, route naar belangrijke zones en contactpunt voor hulp of meldingen.
- Bescherm spawn, infrastructuur en andere gemeenschappelijke bouwwerken tegen ongewenste wijzigingen. Leg vast wie bouwrechten heeft en hoe studenten een bouw- of projectzone aanvragen.
- Werk met een heldere wereldstructuur, bijvoorbeeld `hub`, `survival` en `beheer/test`. Leg de functie, toegang en reset- of behoudsbeleid van elke wereld vast.
- Stel de serverregels op in overleg met de docent. Neem minstens respectvol gedrag, griefing, cheats, privacy, rapportering en gevolgen bij overtredingen op. Maak ze zichtbaar in de hub en bewaar de bronversie in de repo.
- Gebruik geen persoonlijke gegevens in borden, logs, screenshots of publieke BlueMap-markers tenzij de betrokken persoon daar uitdrukkelijk mee instemt.

## BlueMap

Voorzie BlueMap zodat spelers de omgeving kunnen verkennen, met aandacht voor privacy en performantie.

- Kies en documenteer het publicatiemodel: intern, via reverse proxy, via VPN of publiek na toestemming van de docent.
- Beperk toegang tot beheermogelijkheden; publiceer nooit onnodige serverbestanden of directory listings.
- Richt alleen nuttige markers in, zoals hub, openbare projecten en belangrijke locaties. Publiceer geen gevoelige locaties, beheerpaden of privébases zonder toestemming.
- Plan renders buiten piekuren, volg CPU, RAM, diskruimte en rendertijd op, en documenteer hoe je een render veilig pauzeert of herneemt.

## Prestaties en duurzaamheid

Optimaliseer aantoonbaar, niet blind. Meet eerst een beginsituatie, wijzig één of enkele gerelateerde instellingen en meet opnieuw.

- Stel redelijke view- en simulation-distance in op basis van het resourcebudget en test dit met meerdere spelers of gesimuleerde belasting.
- Beperk onnodige entities, redstone-klokken en zware farms via duidelijke spelregels en waar nodig proportionele serverinstellingen.
- Beheer de wereldgrootte: kies een wereldborder, pre-generate relevante chunks indien haalbaar, en documenteer de impact op opslag, back-up en BlueMap-renders.
- Houd server, Java-runtime en plugins actueel via een geplande change. Test updates eerst in de testwereld of een tijdelijke kopie en houd een rollbackpad klaar.
- Leg een onderhoudsvenster, escalatiepad en overdrachtsmoment vast. Het doel is continuïteit, geen afhankelijkheid van één student.

## Rollen en verantwoordelijkheden

Maak in `groepsindeling.md` of een gekoppeld document een actuele verantwoordelijkenmatrix. Rollen mogen gecombineerd worden in kleine groepen, maar elke kritieke taak heeft minstens een eigenaar en een back-up.

| Rol | Kernverantwoordelijkheid | Niet toegestaan zonder change/goedkeuring |
|---|---|---|
| Service owner | roadmap, capaciteit, overdracht en afstemming met docent | alleen beslissen over ingrijpende wijzigingen |
| Platformbeheerder | VM/container, updates, serviceproces, back-up en restore | zichzelf of anderen onnodige spelrechten geven |
| Netwerk- en securitybeheerder | OPNsense, DNS, firewall, VPN en toegangscontrole | beheerpoorten publiek maken |
| Wereld- en hubbeheerder | spawn, beschermde zones, bouwrichtlijnen en wereldstructuur | sancties of permanente verwijderingen zonder procedure |
| Moderator | rapporten behandelen, chat/spelgedrag opvolgen en incidenten registreren | platform- of netwerkbeheer, verborgen surveillance |
| Docent/sponsor | beleid, uitzonderingen, escalaties en continuïteit bewaken | dagelijkse spelersmoderatie overnemen tenzij nodig |

Gebruik least privilege. Maak aparte accounts voor beheer en normaal spelen; deel geen accounts. Beperk operatorrechten tot een zeer kleine, gemotiveerde groep. Documenteer alle rollen, rechtenplugins/groepen en de procedure voor toekennen, intrekken en periodiek herzien van rechten. Bewaar credentials uitsluitend in Bitwarden of het goedgekeurde alternatief.

## Operations en overdracht

- Maak een runbook met start/stop/restart, veilige update, spelersmelding, back-upcontrole, restore en incident-escalatie.
- Maak minstens dagelijkse wereldback-ups en bepaal retentie volgens het beschikbare opslagbudget. Back-ups moeten consistent zijn: stop of flush de wereld volgens de gekozen servermethode voordat bestanden worden gekopieerd.
- Voer minstens één restore-test uit naar een geïsoleerde testlocatie en leg resultaat, duur en eventuele dataverliesgrens (RPO) vast.
- Monitor minstens beschikbaarheid, spelersaantal, CPU, RAM, diskruimte, server-TPS/tickduur en back-upstatus. Centraliseer relevante logs en beperk hun toegang.
- Registreer wijzigingen, storingen, sancties en belangrijke beslissingen met respect voor privacy. Gebruik bestaande change- en incidenttemplates waar mogelijk.
- Stel een korte overdrachtsgids op voor het volgende cohort: architectuur, toegang aanvragen, dagelijkse taken, open risico's, onderhoudskalender en contactpersonen. Laat minstens één student buiten het primaire beheerteam een herstel- of beheertaak uitvoeren op basis van die gids.

## Vereist bewijs in de repo

- architectuur- en netwerkdiagram met de Minecraft-server, BlueMap en toegangsgrenzen;
- servicefiche volgens [de servicetemplate](templates/service-template.md);
- rollenmatrix en actuele contact-/backupverantwoordelijkheden;
- regels en screenshots van hub/spawn, zonder gevoelige informatie;
- BlueMap-publicatiemodel, relevante configuratiekeuzes en renderplan;
- vóór/na-meting van minstens één optimalisatie, met conclusie;
- firewall-, NAT- en rechtenvalidatie, inclusief een negatieve test voor een niet-toegelaten toegang;
- back-up- en restore-test, monitoringbewijs en minstens één operationeel change- of incidentrecord;
- overdrachtsgids en lijst met openstaande verbeterpunten.

## Acceptatietest voor de demo

1. Een gewone speler kan via de afgesproken weg verbinden en komt veilig in de hub terecht.
2. Die speler kan geen spawn, beheerzone of serverinstellingen wijzigen.
3. Een moderator kan een melding volgens procedure registreren, zonder platformbeheerrechten te krijgen.
4. Een beheerder toont een veilige update- of restartprocedure en controleert nadien de serverstatus.
5. BlueMap toont uitsluitend wat volgens het gekozen publicatiemodel zichtbaar mag zijn.
6. De groep toont monitoring en een geslaagde restore-test.
7. Een andere student kan met het runbook een afgesproken routinehandeling uitvoeren.

