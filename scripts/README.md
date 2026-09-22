# Scripts

Bewaar hier scripts die jullie zelf gebruiken voor beheer, controle of automatisatie.

Regels:

- scripts moeten leesbaar en veilig zijn;
- geen secrets hardcoden;
- documenteer doel en gebruik;
- gebruik veilige defaults;
- test scripts voor je ze op belangrijke systemen uitvoert.

Voor scripts die iets wijzigen:

- voorzie waar zinvol een dry-run en bevestigde doelomgeving;
- stop bij fouten in plaats van blind verder te gaan;
- schrijf bruikbare logs zonder secrets;
- documenteer idempotentie, rollback en minimale rechten;
- laat een groepslid de wijziging reviewen.
