# Spelregels voor Smith

Deze regels beschermen de productieomgeving, het campusnetwerk en de gegevens van gebruikers.

## Alleen binnen jullie scope

Studenten mogen binnen de toegewezen Proxmox-pool:

- VM's maken, configureren, starten, stoppen en verwijderen;
- besturingssystemen en projectsoftware beheren;
- eigen applicatieaccounts en rollen beheren;
- goedgekeurde back-up-, monitoring- en automatiseringskoppelingen gebruiken.

Alles buiten die pool of buiten het toegewezen netwerk blijft buiten scope.

## Absoluut niet toegestaan

- instellingen van Smith, gedeelde storage, bridges of andere pools wijzigen;
- workloads, verkeer of accounts van andere groepen bekijken of testen;
- rogue DHCP, router advertisements, spanning tree of routing aanbieden;
- het campusnetwerk scannen, belasten of omzeilen;
- een dienst publiek maken zonder goedgekeurde change;
- secrets, persoonsgegevens of ongeschoonde exports in Git opslaan;
- illegale software, auteursrechtelijk materiaal of ongeautoriseerde game-images verspreiden;
- mining, cryptomining, botnets, offensieve tooling buiten een goedgekeurde geïsoleerde CTF-scope;
- destructieve of belastende tests uitvoeren zonder plan, tijdslot en akkoord.

## Verplicht

- least privilege voor Proxmox, OS en applicaties;
- een hostfirewall en doelgerichte netwerkregels;
- ondersteunde software en tijdige security-updates;
- unieke serviceaccounts en secrets in de afgesproken vault;
- monitoring van beschikbaarheid en resourcegebruik;
- back-up van niet-reproduceerbare data en minstens één hersteltest;
- logging van changes, incidenten en beheerhandelingen;
- een actueel resourcebudget en VM-register;
- verwijdering of overdracht van testaccounts en tijdelijke data na afloop.

## Stopregel

Stop de actie en verwittig de docent bij onverwachte impact op Smith of het campusnetwerk, vermoeden van datalek, verlies van beheercontrole, plots hoog resourcegebruik of twijfel over toestemming. Snel en transparant melden weegt zwaarder dan een fout verbergen.
