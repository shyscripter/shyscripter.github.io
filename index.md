# Karting League - Version 3.5.0

## New Additions
```md
- Added a display for the amount of time left during intermissions between races
  * This was never intended to be removed from the game and has been re-introduced during a recode of the core game loop to fix multiple oversights (including this one :P)

- The lobby music has been changed and reacts when you open/close a menu in the lobby
  * For those who preferred a previous iteration of the lobby theme, we may introduce some form of personalization in the future after higher-priority features get implemented

- Added a button in the settings menu to reset controls to their default keybinds
  * Clicking the button once will reset controls for all input devices, not just the one you're currently using
  * Existing keybinds are not erased. If you at any time wish to use default keybinds, reset keybinds by clicking the button in the controls page of the settings menu
  * I recommend resetting your controls to the new default keybinds because a lot has changed!

- Karts can now switch directions during a drift
  * Quickly release the drift button while holding the opposite direction then hold the drift button again
  * You can repeat this as many times as you want and still hold one continuous drift
  * Doing this will remove a bit of your current charging drift boost. The current drift cannot downgrade to a lower tier in cases where the current tier's charging progress is low

- Tricking has been completely overhauled to allow multiple tricks per jump for extra mechanical depth
  * Trick boosts start as strong as blue drifting boosts
  * Each successful trick in a row upgrades the boost's tier
  * Any consecutive tricks past three in a row are purely for style, tricking cannot give you a boost stronger than that of a purple drift
  * It is now possible to fail tricks if the kart lands on the ground before the trick animation is complete
  * Failed tricks give no boost and kill all current momentum (does not stun you)

- Most items can now be used in two different ways, with their main fire or their alternative fire
  * Hazards can be deployed behind your kart or thrown forward
  * Projectiles can be sent forwards or backwards
  * Other items only have one mode of fire
  * For mobile players, the game will automatically decide which mode of fire to use when pressing the item button

- Removed the teleporter to trading servers, making the feature no longer accessible
  * We have gone forward with the voted upon decision to remove trading from the game
  * We don't have proper compensation ready yet! But you will get some special things in the next update when we add customization

- The following karts have been added to the game: Deskjet, Sky Wave, Night-shifter, Geisha, Magnus, Ice Screamer, Turbo Tyke, Hampster, Travel Chaldron

- The following karts have received remodels: Sunburst Roadster, Phoenix, Stallion, Boomboxer, Slingshot, Go-Wagon, Patriot, Ghille Jeep, Duality, Technisch, Breadwinner, Super Unicorn, Speed Box, Deja 86, Standard Kart (for the final time, trust)
```
## Small Changes
```md
- Maps use a new node system instead of needing "ItemWaypoints" and "Respawns" folders to be made separately
* Expect the track kit and the custom tracks game to be updated sometime soon
* The custom tracks game will not be backwards compatible. If you wish for older tracks to be playable, update your tracks when the track kit and custom tracks game get updated

- Removed Banland Stadium, Castle In The Sky, Crossroads, Downtown, Freemodel Freeway, Kry Isle, (Legacy) Track Kit, Oasis Desert, Poisonous Grove, Red Planet, Snowfall Circuit, Thunderstorm Fortress, and Wild Wild East from the secret track pool, resulting in them all being vaulted until they get reworked
  * Due to their lack of popularity in their current forms and the fact that these tracks were already put in the secret track pool, the current versions of these maps are not worth maintaining when these are already going to be the first tracks that get remodeled in the future
  * All of these tracks will eventually return in some way, but we need time to deliver their remodels over the course of several updates

- If a server's core game loop ever throws an error, the server will shut itself down. Data is saved as this happens to prevent unintentional data loss in the event of a crash

- For keyboard only, assigned new default keybinds:
  * Q/E for main item usage/alt item usage
  * Space for drifting
  * Left Ctrl for brakedrifting
  * Left Shift for looking backwards

- Left/right clicks from the mouse are now supported for main/alt item usage respectively

- Lowered the opacity of the rain in Master Speedway to improve visibility without ruining the track's theme

- Removed the constant spinning of all karts in the menu to improve game performance in the lobby, but now a new animation will play when selecting a kart

- Added new sounds in the menu that play when attempting to select/buy karts

- Terrain particles will now only render for your own kart
  * This is a side effect of a recode of this particle system
  * Intended to improve game performance when more karts are on the map at once

- Improved animations of karts when getting stunned

- Changed the game's lighting style from Realistic to Soft
  * Reverting a previous change because this ended up being a downgrade to the game's graphics
  * All current tracks were given lighting with the Soft style in mind and they look better with this lighting compared to the Realistic lighting style
  * We will go back to Realistic lighting when every track gets changes to their lighting to be a full on graphical upgrade

- Improved the VFX of the speed lines

- Moved the drift bar from the bottom of the HUD to where the vehicle is on the screen and made it vertical

- Altered a few existing driver animations to adjust priority internally
  * Completely redid the panic (getting hit by an item) animation to be consistent across all vehicle types and to make it more obvious that the driver is losing control of the vehicle

- Added new driver animations for item holding and usage

- Item Boxes have been remodeled

- Your driver will now cheer when hitting someone with an item

- AI drivers have been removed for the time being. They need a recode that wasn't able to be started on this update

- For our collective sanity, the random vote option can no longer pick secret tracks in public servers
```
## Balance Changes
```
- Lightning (now Lightning Rod) now only hits drivers that are ahead of the user instead of hitting every player on the track
  * This is intended to help the Lightning Rod help bring the pack closer to each other rather than unnecessarily slow down players who are already very far behind

- Item Scrambler now grants temporary invulnerability upon use and was reworked to steal its target's item instead of deleting it
  * Deleting items out of existence does not benefit the Item Scrambler's user. This is intended to help the Item Scrambler feel less underwhelming and have a distinct purpose

- Forcefield (now Shield) can now only protect against one hit instead of giving temporary invulnerability
- Shield can now block lightning
  * Done to help the shield have a distinct purpose now that more items can be used defensively
- Shield lifetime increased from 10s -> 20s

- Time Bomb (now Dynamite) blast radius reduced from 50 -> 25 studs
- Dynamite can now detonate upon contact with a kart
  * The blast radius was way too large and made it nearly impossible to dodge a perfectly timed trap
  * Instead of relying on a specific timing, detonation is intended to allow this item to be used offensively like the other hazard items

- Some items now have global cooldowns that apply when the race starts and when the item is last used

- Some items now have a maximum amount of players that can hold them at once
```
## Bugfixes
```md
- Fixed a small jump on Shattered Sky that caused players to get stuck on the landing platform near the end of the track

- Fixed an issue that caused starting a drift when airborne to lock the vehicle's steering until the button is released

- Fixed a visual bug where players who own the extra vote pass show up on the voting menu twice for a split second

- Fixed an issue that caused karts to not face the correct direction upon respawning

- Fixed an issue that prevented the camera from focusing on a new character when attempting to spectate other drivers

- Brought back the background blur that was supposed to show up when opening a menu, the lack of one was a bug with the map lighting system

- Gravity alignment has been capped to 60 FPS, intended to fix weird alignment behavior at high framerate

- Fixed issues with kill planes on Talora Dustwoods and Desert At Dawn
```
## [Enjoy and play here!](https://www.roblox.com/games/9416437817/Karting-League)
