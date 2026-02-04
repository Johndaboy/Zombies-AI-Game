# Design Document - Zombies AI Game

## 1. Tech Stack (Unity)
- Game Engine: Unity (3D)
- Programmeertaal: C#
- Input: Unity Input System (of standaard Input Manager)
- AI / Navigation: Unity NavMesh (voor zombie pathfinding)
- UI: Unity UI (Canvas + TextMeshPro)
- Data: ScriptableObjects (voor weapons, prijzen, stats)
- Versiebeheer: Git (bijv. GitHub)

## 2. Globale Architectuur
- De game is opgebouwd uit losse systemen die samenwerken via duidelijke verantwoordelijkheden.
- Belangrijkste componenten:
- GameManager
- Regelt de game state (start, wave, game over)
- WaveSystem
- Beheert wave nummer, scaling en wanneer nieuwe zombies spawnen
- ZombieSpawner
- Spawnt zombies op vaste spawnpoints buiten de arena
- ZombieAI
- NavMesh movement richting speler
- Aanvallen, barricades slopen, target switching
- PlayerController
- Movement, shooting, reload, interacties
- PointsSystem
- Punten toevoegen en uitgeven
- Interactables
- Deuren, barricades en wall buys via een gedeeld interactie-systeem

## 3. Belangrijke keuzes
- Interactable systeem
- Deuren, barricades en wall buys gebruiken één uniforme interface (Interact()) zodat uitbreiding makkelijk blijft.
- ScriptableObjects voor wapens
- Wapens worden data-driven gemaakt (damage, ammo, prijs), zodat je makkelijk nieuwe wapens toevoegt zonder code te herschrijven.
- NavMesh voor zombie movement
- Snelle en betrouwbare manier om zombies naar de speler te laten lopen, zonder zelf pathfinding te bouwen.
- Wave scaling simpel houden
- Waves worden groter en zombies krijgen meer HP. Dit voorkomt dat balancing te complex wordt.

## 4. Bekende risico’s
- Zombie pathfinding bugs
- Zombies kunnen vastlopen of rare routes nemen als de NavMesh niet goed is gebaked of als deuren dynamisch openen.
- Balancing problemen
- Punten, weapon prijzen en wave difficulty kunnen snel te makkelijk of te moeilijk worden.
- Performance issues
- Te veel zombies tegelijk kan FPS drops veroorzaken, vooral bij slechte object pooling.
- Scope creep
- Extra features zoals perks, mystery box, verschillende zombie types kunnen het project groter maken dan haalbaar.