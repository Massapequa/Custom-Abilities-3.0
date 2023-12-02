# Custom-Abilities-3.0
Easier implementation, more customization, more abilities!<br>
<br>
Custom Abilities for the ServUO Ultima Online emulator (www.ServUO.com).<br>
<br>
Be aware that all of these abilities are being tested on ServUO-57.1 At the time of writing this, there is a newer version released and these abilities should, for the most part, work with it. However, if there are any conflicts with your version, feel free to post on the thread or direct message me on the ServUO forums. I'd be happy to try and help with any issues you might be having. I want nothing more than for those reading this to have fun with the wrok I've created. We've already solved a number of issues on the thread that people have had with 1.0 and 2.0, and maybe the solution to your issue is already there.<br>
<rb>

<details>
<summary> <b>Implementation changes:</b> </summary>
	AbilityCreature and AbilityMount have been added as extensions to the BaseCreature class.<br>
	This allows everyone to more easily add CustomAbilities to your creatures.<br>
	You no longer need to mess with the OnThink() method in order to make the abilities work.<br>
  <br>
	WARNING: remove all current instances of your spawned creatures before changing them from BaseCreature to AbilityCreatures.
</details>

<details>
<summary> <b>New 3.0 Abilities:</b> </summary>

Fear: Pets flee in terror and players are frozen in fear!

Summon Minion: The creature summons an ally to help them in combat!<br>
		the look, sound, and effects of the summoned minion can be customized.

Forked Flame Strike: Sends out a three pronged attack of cascading flamestrikes!<br>
		Has the typical elemental 'Type' options of all FlameStrike abilities.

Snare: Sends out a projectiile that holds the target in place!<br>
		The projectiile, sound, and image ID that appears on the target can be customized.
		By default, Snare traps the player in a giant spider web.
</details>

<details>
<summary> <b>Bug fixes and edits:</b> </summary>

-Firebolt, Geyser, and all FlameStrike variations:<br>
		All abilities with a 'Type' option now include the 'Blood' Type.
		the Blood Type has deep red hued effects with 100% physical damage.

-Flame Strike Cone and Flame Strike Line:<br>
		Tamed creatures no long damage themselves and other pets while using these abilities.

-Heal Allies:<br>
		 Now can be used outside of combat.

-Ice Prison:<br>
		Added the ItemID, Hue, and sound properties.

-Zap:<br>
		Added the ItemID, Hue, and sound properties.

-Impale Aoe:<br>
		Added the ItemID, and Hue Properties.

-Flame Burst:<br>
		Added the Hue property.

-Blizzard:<br>
		Now has the elmental 'Type' option like Firebolt and the FlameStrike abilities.
		the options include: fire, ice, poison, energy, water, snow, necrotic, holy, and blood.
  </details>

Here is a list of all of the abilities and their customizable attributes:

## Ability Attributes
<details>
<summary>
Click to reveal list of all of the abilities and their customizable attributes:
</summary>

### FlameStrikeTargeted
- **Type**: (Fire, Ice, Poison, Energy, Water, Steam, Necrotic, Holy, Blood)
- **Usage**: `ability.Type = FlameStrikeTargeted.StrikeType.` *Element goes here*
- **SetDamage**: 12 - 16 by default.

### Charge
- **SetDamage**: 12, 16 by default.

### FlameStrikeAoe
- **Type**: (Fire, Ice, Poison, Energy, Water, Steam, Necrotic, Holy, Blood)
- **Usage**: `ability.Type = FlameStrikeAoe.StrikeType.` *Element goes here*
- **Range**: 5 by default.
- **SetDamage**: 12, 18 by default.

### Firebolt
- **Type**: (Fire, Ice, Poison, Energy, Water, Steam, Necrotic, Holy, Blood)
- **Usage**: `ability.Type = Firebolt.BoltType.` *Element goes here*
- **SetDamage**: 8, 12 by default.
### Ambush
- **SetDamage**: 12, 24 by default.

### Geyser
- **Type**: (Fire, Ice, Poison, Energy, Water, Steam, Necrotic, Holy, Blood)
- **Usage**: `ability.Type = Geyser.GeyserType.` *Element goes here*
- **Message**: Message that's sent when a player is caught in the blast.
- **SetDamage**: 18, 24 by default.

### IcePrison
- **SetDamage**: 0 by default.

### WalkingBomb
- **SetDamage**: 18, 26 by default.

### MeteorStrike
- **Message**: Message that's sent when a player is struck.
- **SetDamage**: 18, 24 by default.

### MeteorShower
- **SetDamage**: 14, 18 by default.

### Thunderstorm
- **SetDamage**: 6, 10 by default.

### ThrowBoulder
-**ItemID**: Change the ID of the projectile.
-**Hue**: Change the object's hue. 
- **SetDamage**: 12, 16 by default.

## Zap
-**ItemID**: Change the ID of the projectile.
-**Hue**: Change the object's hue. 
-**Sound**: Electrical sound when hit.
- **SetDamage**: 8, 12 by default.

### ToxicRain
- **SetDamage**: 9, 18 by default.
- **Hue**: 64 by default.

### ToxicSpores
- **SetDamage**: 21, 28 by default.
- **Range**: 5 by default.

### ImpaleAoe
- **Range**: 5 by default.
- **ItemID**: Change the ItemID of the item that appears on the target. (A random stalagmite by default.)
- **SetDamage**: 12, 18 by default.

### FlameStrikeLine
- **Type**: (Fire, Ice, Poison, Energy, Water, Steam, Necrotic, Holy, Blood)
- **Usage**: `ability.Type = FlameStrikeLine.StrikeType.` *Element goes here*
- **Range**: 5 by default.
- **SetDamage**: 16, 20 by default.

### BarrageOfBolts
- **ItemID**: Change the ID of the projectiles.
- **Hue**: Change the hue of the projectiles.
- **Sound**: Fireball sound by default.
- **SetDamage**: 12, 18 by default.

### FlameStrikeCone
- **Type**: (Fire, Ice, Poison, Energy, Water, Steam, Necrotic, Holy, Blood)
- **Usage**: `ability.Type = FlameStrikeCone.StrikeType.` *Element goes here*
- **Range**: 5 by default.
- **SetDamage**: 16, 20 by default.

### Grapple
- **Emote**: Message that appears over the creature's head as it casts the ability.
- **Range**: 5 by default.
- **SetDamage**: 3, 8 by default.

### ThrowExplosives
- **Hue**: Change the hue of the projectile.
- **Duration**: Change the duration of the fire left on the ground after impact. (10 seconds by default.)
- **SetDamage**: 10, 20 by default.

### ThrowTimedExplosives
- **Message**: Message that displays when a player is hit by the blast.
- **ItemID**: ID of the projectile and item placed on the ground.
- **Sound**: Sound when the bomb detonates.
- **SetDamage**: 32, 40 by default.

### HealAllies
- *Note*: In order to make specific creatures healable allies, you must update the casting creature's IsFriend() method.
- **Range**: 12 by default.
- **SetHealing**: 10, 18 by default.

### FlameBurstAoe
- **Range**: 5 by default.
- **SetDamage**: 28, 34 by default.

### RagingTempest
- **SetDamage**: 8, 16 by default.

### Blizzard
- **Type**: (Fire, Ice, Poison, Energy, Water, snow, Necrotic, Holy, Blood)
- **Usage**: `ability.Type = Blizzard.StormType.` *Element goes here*
- **SetDamage**: 12, 18 by default.

</details>


## 1.0 Abilities:
  
### Flame Strike Targeted
- **Description**: Casts a Flame strike on the target, with elemental customization options.

### Charge
- **Description**: The monster charges at the player from a distance, with customizable range.

### Flame Strike Aoe
- **Description**: Creates a circle of flame strikes around the monster, damaging all players and pets within. Customizable range and elemental effects.

### Firebolt
- **Description**: Fires a simple fireball at the target, with elemental customization.

### Ambush
- **Description**: Monster vanishes and reappears at the target's location to deliver a damaging attack.

### Geyser
- **Description**: Creates a swirling pool beneath the player, followed by a large geyser eruption. Players can avoid the blast by moving. Customizable elemental effects.

### Ice Prison
- **Description**: Traps the target in a block of ice for a short duration, with options to customize the hue and item ID.

### Walking Bomb
- **Description**: Marks a target before an explosion erupts, damaging nearby players. 

### Meteor Strike
- **Description**: Summons a shadow over a target player, followed by a crashing meteor. Players can avoid the damage by moving in time.

### Meteor Shower
- **Description**: Calls down a flurry of meteors at random locations near the target.

### Thunderstorm
- **Description**: Strikes all nearby targets with lightning.

### Throw Boulder
- **Description**: The creature hurls a large boulder at a target location, hitting and briefly knocking down any player in the area.

### Zap
- **Description**: Sends out a bolt of electricity that temporarily paralyzes the target.

### Toxic Rain
- **Description**: Douses the target in toxic rain, leaving pools of acid in their wake.

### Toxic Spores
- **Description**: Creates a circle of exploding mushrooms around the target, damaging anyone in the area and leaving pools of acid.

### Impale Aoe
- **Description**: Causes stalagmites to erupt from the ground, piercing anyone in the area and inflicting bleeding. Customize the hue and item ID of the stalagmites.

### 2.0 Abilities:

| Ability                | Description                                                                     |
|------------------------|---------------------------------------------------------------------------------|
| Flame Strike Line      | Sends out cascading flames in a direct line toward the target. All enemies in the way get damaged. |
| Barrage Of Bolts       | Sends a flurry of firebolts at a target. Any enemy caught in the location gets damaged. |
| Flame Strike Cone      | Creates a massive cone of fire in front of the creature that damages all nearby enemies. |
| Grapple                | The creature pulls the target towards them.                                  |
| Throw Explosives       | The creature throws a small explosive that hits the target and leaves a small fire behind. |
| Throw Timed Explosives | The creature throws an explosive barrel at the target that detonates after a short time and damages all nearby targets. |
| Heal Allies            | Heals nearby allies.                                                           |
| Flame Burst Aoe        | Creates a large area of effect blast at the creature's location and leaves behind flames in the blast zone. |
| Raging Tempest         | Creates a prolonged thunderstorm in an area by the target.                   |
| Blizzard               | Creates a massive storm at the creature's location.                          |
