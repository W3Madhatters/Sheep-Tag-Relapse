# Sheep Tag: Relapse

Sheep Tag: Relapse is a Warcraft 3 map that traces its roots back to the original Sheep Tag maps, but more recently, to Sheep Tag Revolution.

This repository holds the Wurst code base that is compiled into the actual Wacraft 3 map. For more information on Wurst, a scripting language that compiles into WC3's JASS, visit https://wurstlang.org/

## Contributing

If you have any ideas for new items/abilities/game modes/balnces or have a bug to report, please submit an issue or start a discussion on the Sheep Tag Community Discord: https://discord.gg/dJuwsc

Feel free to download the code base and mess around with it. Submit a pull request with any changes you think should be included in the game.

## Relapse vs Revolution

The general idea behind Relapse is to take Revolution and remove some of the pain points while hopefully increasing the excitement and making it easier for pubs to ease into. The main changes relate to Terrain, Saving, and Shepherding.

### Terrain

The terrain for Relapse is completely new, but the major difference is in size: Revolution's map is over twice as big. There have been plenty of arguments over how terrain size affects gameplay, but in my mind, it boils down to a small map having the following advantages:
 * Sheep are almost always under threat since there is never a gigantic mass to hide in
   * More threat means more isolations and deaths, which means other gameplay mechanisms can be tweaked to make a Sheep death less crippling (e.g. saving, destroying farms, etc.)
   * Shepherds aren't as easily demoralized when Sheep are always within reach 
 * Sheep have to focus more on intelligent/challenging/teamwork focused gameplay (bridging/harassing/expanding), instead of maximizing their farms per second in one giant corner-mass
 * Sheep cannot run almost endlessly in one direction, dragging out games

 ### Saving

 In my mind, the saving system is currently the largest flaw in Sheep Tag (at least at high levels). Not only are Sheep mostly safe to AFK the rest of the round after a death, a Shepherd is forced to stop all useful/fun actions just to watch them. The difficulty of saving combined with the extreme punishment of dying (losing farms + one less Sheep producing farms in a game that is currently largely focused on sheer quantity of farms on the map) means that many games are determined almost solely by when the first sheep dies.

 The current saving system in Relapse does not involve the pen at all. Instead, dying sheep will turn into spirits that can move around the map, and will eventually turn back into sheep (the time to revive increases with each death).

 I believe this system offers the following advantages:
  * No player (on either team) is excluded from gameplay after a death
  * Since revival is automatic, sheep deaths are far less catastrophic, allowing the game to be designed in a way that encourages more threat to sheep
  * Newer players will have multiple attempts at playing sheep, instead of the current situation where they normally die early and remain dead

### Shepherding

Currently Shepherds have no critical decisions or interesting abilities... They basically just melee farms to death then buy claws to melee them to death faster, while the interesting items like golem, strength, and beam, go unused because they're objectively worse decisions in the long run.

Relapse attempts to fix this by removing the majority of current items, and turning Shepherds into heroes with abilities. As Shepherds level up, they will gain damage, and also get to select from a set of hero abilities (some similar to current items, some new). This means that Shepherds aren't presented with the "choice" between getting what's fun or what's smart, and the game can be balanced around them having both.

Items are still available, but now focus more on utility (e.g. cooldown reduction), rather than playing an extremely critical role.

Shepherds can currently choose from one of two heroes:

Shepherd:
 * Base Abilities:
    * Mirror Image
    * Summon Golem
 * Upgrade: Reinforce - Causes Mirror Image to target a point, to which the image will be sent
 * Upgrade: Iron Golem - Increases the damage and duration, while reducing the cooldown of Summon Golem
 * Passive: Cleave - Causes attacks to damage farms in a line beind the targeted farm
 * Torch - Burns an area, dealing initial damage to farms, and catching some on fire, causing them to take damage over a long period of time
 * Demolition - Target a farm to cause it to explode after a short delay, slowing any sheep nearby

Wolf:
 * Base:
    * Mirror Image
    * Impale - On next attack, cast a wave of thorns that damage farms and stun sheep in a line behind the farm
 * Upgrade: ?? - Increases the speed of mirror image and allows it to travel over multiple farms
 * Upgrade: ?? - Increases the damage, range, and stun duration of Impale while reducing the cooldown
 * Passive: Frenzy - Grants temporary movement, attack speed, and damage after casting any spell
 * Juggernaut - Temporarily greatily increases damage at the cost of movement and attack speed
 * Summon Pack - Summons extremely short lived wolves that can only target sheep, but are fast

 ### Other Noteworthy Changes

 * By default, the game will open with very basic host options (e.g. setting the number of rounds/game mode) then end after those rounds have finished. This is both to make the game more user-friendly, and to encourage games to be remade more often, allowing more people to join and experience the game. There will be a command to allow the game to be set up/played as it normally is in Revolution
 * The portable shop will likely be removed. Buying items with chat commands (and chat commands in general) is a poor user experience, and since items are no longer as critical to gameplay, it feels unnecessary.
 * Shepherds will start with 4-hit kills on farms. With the small terrain size, and access to abilities, Shepherds should not need to start with 2 or even 3-hit kills on farms. As Shehpherds level, they will gain increased damage, eventually dealing enough damaage to 2-hit farms, but 1-hit will be impossible (without abilities). Upgraded farms may have their health reduced to 50% more than regular farms (instead of 100% more).