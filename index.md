# Karting League - Version 3.6.0

## New Additions
```md
- Vehicles now react to changes in momentum in each direction, including collisions

- When starting a race, a new minigame has been added to determine the boost you get

- The vehicle's traction is now affected by the terrain type that it's driving on. Vehicles with a high Off-Road stat can mitigate traction loss
  * This is intended to give Off-Road vehicles a more solid niche than mowing through corner cuts, and to allow tracks on different terrain to play slightly differently
  * When under the effects of a Cola/Boost Pad boost, traction loss is cut by a factor of 4
  * Traction loss is cut in half when under the effects of a Power Orb. Stacks with previously mentioned boosts

- You can now perform rolling burnouts when holding gas and brake at low speeds
  * Also hold drift to perform a static burnout

- Reworked the vehicle engine sound system to use proper gearing and a separate idle sound

- Added announcer voice lines that react to how you finish the race

- Transformation between car, boat, and plane physics has been implemented. These are currently not accessible in the main game because we need tracks that are designed with these new mechanics in mind to officially add them
  * This is an open beta for CT creators to mess around with the transform mechanics and understand how they work in advance so they can begin making tracks with the new mechanics in mind
  * The visual effects of transforms are not here yet, but they are fully functional. Model changes and additions are a feature we intend to add in the next update when transforms have the content they need in order to officially release into the main game
```
## Small Changes
```md
- Loading screen now smoothly fades in from a black screen when joining the game

- Refactored the entire game's backend to use a single script architecture model
  * This doesn't really change anything at all for you guys, but it makes it leagues easier for us to add new features and fix bugs due to centralizing where code lives

- Karts now lose speed more gradually when letting go of the accelerate button and when braking

- A proper sound of nitrous (de)activating now plays when karts begin/end to boost

- Switched the drifting tiers of orange and blue boosts primarily to spite Kiwi
  * Now it's scientifically accurate!

- All tires now emit tire marks on the ground when drifting. Only the rear tires still emit smoke particles, which have been redesigned
  * These effects are global and can be seen by all players

- Due to the way i patched the "you face the wrong way when spawning into a track" issue, you can no longer move around during a race's startup

- A bar now appears above your character when pressing the respawn button, indicating that you need to hold the button to respawn manually

- When racing in time trials, the kart will now spawn in the center of the starting grid instead of the left

- Changed the final lap and next lap sounds

- Merged the CT codebase and the base game codebase into one, which should make future updating of CTs faster
  * The Custom Tracks game is back up too! The track kit has been updated to include the new stuff that came with the update
```
## Balance Changes
```
- When hit by a tumbling stun tier item, you now lose your speed over a short time instead of being instantly stopped. Being instantly stopped is now solely reserved for the explosion stun tier
  * During the initial item rework, Seeker Missiles (and its variants) were a little too punishing but directly nerfing them would harm the game's balance more than it would help
```
## Bugfixes
```md
- Fixed an issue that caused the player to see a black screen when colliding with walls in strange ways

- Corrected the categorization of walls on multiple tracks that were not supposed to be alignable

- Lowered some killplanes that are too high on multiple tracks

- Added a killplane in FM Vista to an unintentionally accessible area that traps you inside (if you don't manually respawn)

- Added a missing rainbow script on the Power Orb's held item model

- The lobby now correctly toggles its visibility when entering/leaving it due to previously being stalled infinitely by old code

- Corrected boost feedback from drifting (wheelies and character movement), since it would always react as if the boost was a purple boost regardless of the actual boost tier the driver boosted with

- Added missing checks that were supposed to prevent the vehicle from starting a drift/switch drifting when in the air
  * You can still hold a drift in the air if you started one when on the ground

- You now finally face the correct direction when spawning into the track

- Added a new check during the map flyover indented to fix an issue where the loading screen does not transition to the cutscene
  * If this issue continues to exist, please make a bug report about it!
```
## [Enjoy and play here!](https://www.roblox.com/games/9416437817/Karting-League)
