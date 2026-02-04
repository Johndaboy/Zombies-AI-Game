# prompts

## creatie van de volgende 2 prompts
maak een prompt voor een soort gelijke call of duty zombies game. met deuren die geopend kunnen worden met geld, muren waar zombies doorheen kunnen komen om de arena binnen te gaan, je character dat de muren kunnen repareren of de deuren kunnen openen maar ook de zombies neer kunnen schieten en geweren kunnen kopen vanaf verschillende paywalls

-- chatgpt prompt 1 --

## class diagram
Maak een Mermaid UML class diagram voor een wave-based zombie survival game geïnspireerd op Call of Duty Zombies.

#### Gebruik de volgende classes en relaties:
##### Classes (met attributen + methods)
- GameManager
- waveNumber:int
- zombiesAlive:int
- pointsSystem:PointsSystem
- waveSystem:WaveSystem
- StartGame()
- StartWave()
- EndWave()
- GameOver()
- WaveSystem
- currentWave:int
- maxZombiesAlive:int
- SpawnWave()
- IncreaseDifficulty()
- ZombieSpawner
- spawnPoints:List<SpawnPoint>
- SpawnZombie()
- SpawnBatch()
##### Zombie
- health:int
- damage:int
- speed:float
- target:Player
- MoveToTarget()
- Attack()
- TakeDamage(amount:int)
- Die()
##### Player
- health:int
- points:int
- currentWeapon:Weapon
- inventory:List<Weapon>
- Shoot()
- Reload()
- TakeDamage(amount:int)
- Interact(interactable:Interactable)
##### Weapon
- name:string
- damage:int
- fireRate:float
- magazineSize:int
- ammoReserve:int
- Shoot()
- Reload()
##### WallBuy
- weapon:Weapon
- cost:int
- BuyWeapon(player:Player)
- RefillAmmo(player:Player)
##### Door
- isOpen:boolean
- cost:int
- OpenDoor(player:Player)
##### Barricade
- integrity:int
- maxIntegrity:int
- Repair(player:Player)
- Damage(amount:int)
- IsBroken():boolean
##### Interactable (abstract/interface)
- Interact(player:Player)
##### PointsSystem
- AddPoints(player:Player, amount:int)
- SpendPoints(player:Player, amount:int):boolean
#### Relaties
- Gamemanager gebruikt WaveSystem en PointsSystem
- WaveSystem gebruikt ZombieSpawner
- ZombieSpawner maakt Zombie objecten
- Zombie target Player
- Player heeft currentWeapon (Weapon)
- Player kan meerdere Weapons hebben (inventory)
- Door, Barricade, WallBuy implementeren/erven van Interactable
- WallBuy bevat Weapon
- Player gebruikt Interactable via Interact()
Gebruik goede multiplicities (1, 0..*, etc) en geef inheritance correct weer.

-- mermaid prompt 1 --

## use-case diagram
Maak een Mermaid UML use case diagram voor een wave-based zombie survival game (Call of Duty Zombies-achtig). Actor Player Use cases Start Game Survive Waves Kill Zombies Earn Points Open Door (requires points) Repair Barricade (earns points) Buy Weapon (requires points) Refill Ammo (requires points) Reload Weapon Take Damage Get Downed / Game Over Relationships Survive Waves includes Kill Zombies Kill Zombies includes Earn Points Repair Barricade includes Earn Points Open Door extends Earn Points (want points first) Buy Weapon extends Earn Points Refill Ammo extends Earn Points Take Damage leads to Game Over Player interacts with all use cases Zorg dat het diagram duidelijk is en dat include/extend correct gebruikt wordt.

-- mermaid prompt 2 --