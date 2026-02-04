# user stories

## User Story 1 — Starten van het spel

Als speler wil ik het spel kunnen starten zodat ik een zombie match kan beginnen.
Prioriteit: must

### Acceptatiecriteria:
- Er is een duidelijke “Start Game” knop.
- Bij starten wordt de speler gespawned in de startkamer.
- Wave 1 begint automatisch na het starten.
- De HUD toont punten, wave nummer en ammo.

## User Story 2 — Zombies in waves

Als speler wil ik dat zombies in waves spawnen zodat het spel steeds moeilijker wordt.
Prioriteit: must

### Acceptatiecriteria:
- Zombies spawnen in waves (wave 1, wave 2, enz.).
- Elke wave heeft meer zombies dan de vorige.
- Zombies worden agressiever/sterker per wave (bijv. meer HP).
Een nieuwe wave start pas als alle zombies van de vorige wave dood zijn.

## User Story 3 — Zombies kunnen doden met schieten

Als speler wil ik zombies kunnen neerschieten zodat ik kan overleven.
Prioriteit: must

### Acceptatiecriteria:
- Speler kan schieten met een wapen.
- Zombies verliezen health wanneer ze geraakt worden.
- Zombies gaan dood wanneer health 0 bereikt.
- Speler kan reloaden als het magazijn leeg is.

## User Story 4 — Punten verdienen

Als speler wil ik punten kunnen verdienen zodat ik deuren kan openen en wapens kan kopen.
Prioriteit: must

### Acceptatiecriteria:
- Speler krijgt punten voor hits en kills.
- Speler ziet het actuele puntenaantal in de HUD.
- Punten worden opgeslagen tijdens de match.
- Punten kunnen worden uitgegeven aan deuren en wall buys.

## User Story 5 — Deuren openen met punten

Als speler wil ik deuren kunnen openen met punten zodat ik nieuwe zones kan bereiken.
Prioriteit: must

### Acceptatiecriteria:
- Deuren zijn standaard locked.
- Bij een deur verschijnt een prompt met prijs.
- Speler kan een deur openen als hij genoeg punten heeft.
- Bij te weinig punten verschijnt een melding.
- Een geopende deur blijft open.

## User Story 6 — Barricades repareren

Als speler wil ik barricades kunnen repareren zodat zombies langer buiten blijven.
Prioriteit: must

### Acceptatiecriteria:
- Zombies kunnen barricades beschadigen.
- Barricades hebben een maximum integrity/health.
- Speler kan barricades repareren via interactie.
- Repareren kost tijd en gebeurt stap voor stap (planken).
- Repareren levert punten op.

## User Story 7 — Wapens kopen via wall buys

Als speler wil ik wapens kunnen kopen via wall buys zodat ik sterker word in latere waves.
Prioriteit: must

### Acceptatiecriteria:
- Er zijn meerdere wall buy locaties in de map.
- Elke wall buy heeft een vaste prijs en wapen.
- Speler kan alleen kopen met genoeg punten.
- Bij aankoop krijgt de speler het nieuwe wapen.
- Het wapen werkt direct (schieten, ammo, reload).

## User Story 8 — Ammo refillen

Als speler wil ik ammo kunnen refillen bij wall buys zodat ik niet zonder kogels kom te zitten.
Prioriteit: nice

### Acceptatiecriteria:
- Als speler al hetzelfde wapen heeft, kan hij ammo refillen.
- Refill kost punten.
- Na refill worden reserve ammo en/of magazijn aangevuld.
- Bij te weinig punten verschijnt een melding.