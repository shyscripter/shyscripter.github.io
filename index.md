# Karting League - Version 4.0.0

## New Additions
```md
- Added so many new karts and cosmetics that a system to highlight new additions in the item shops needed to be created
  * We lost track of how many we added and can't be bothered to count this many new entries
  * This includes two new free vehicles: Standard Bike & Standard Quad
  * The Pipe Frame is now free
  * Free vehicles are automatically added to your inventory on login

- Added a new "premium" currency: Vault Tickets
  * Any limited can be purchased with Vault Tickets at any time after the initial spotlight of them being buyable with Credits has ended
  * From now on, new Limited vehicles that go off-sale will be taken out of the shop for the duration of one update. After this offsale period, the vehicle will return to the shop and be buyable with Vault Tickets instead of Credits. This same rule also applies to Daily Streak vehicles after they are sunsetted
  * Players with VIP will earn 1 Vault Ticket for every 500 Credits they earn from races (base rewards only).
  * All players will earn Vault Tickets when leveling up (400 on every 10th level, 300 on every 5th level, 100 on every other level)

- The Stud Racer and Slingshot have been sunsetted, with the new daily streak karts for the next few months being the Tonfa and Slingshot
  * Those who missed out on obtaining the sunsetted karts during their meant availability will be able to purchase these karts in the next update for Vault Tickets!

- Completely redesigned the entire UI

- The minimap has been reworked to show the entire track instead of just what's around you

- Daily Tasks now randomly generate tasks to complete each day instead of always using the same three
  * You can now earn Vault Tickets by completing all three of your daily tasks

- Added a system for one-time redeemable codes, which you can redeem in the new Codes menu
  * New codes will be added to the codes channel daily until we go through all existing codes

- You can now customize your vehicle's colors, materials, wheels, drift, boost, and horn. New cosmetic items for each category have been added to a brand new customization menu
  * Once you purchase a cosmetic item, it is unlocked for all vehicles regardless of the one you had equipped at the time of purchase
  * Equipping cosmetics for a vehicle will only change the appearance of that one vehicle
  * The first limited cosmetic, Galaxy (Drift), is up for grabs! Like we've done for vehicles, limited cosmetics will still be buyable with Vault Tickets after the initial period where it's buyable with Credits ends

- Implemented a daily leaderboard for trophies
  * Trophies are a new thing you earn when completing races. They are not a currency and are reset to 0 daily
  * You can earn Vault Tickets by placing in the top 100 on a daily trophies leaderboard
  * This leaderboard resets at midnight UTC each day and only tracks the trophies you earn each day

- Leaderboards are now displayed in the lobby

- Snowfall Circuit has been completely remodeled and added back into the map pool

- Redesigned mobile controls for (hopefully) the final time
  * We think that this iteration strikes a balance of simplicity and ability to perform every technique in the game

- Reezee's Mansion has been re-added into the map pool
  * We found the issue that caused its position tracking to be messed up

- Added a stats summary inside of the settings menu

- Added a prop debris system that allows karts to smash into objects
  * Doing this will decrease your speed as if you were driving in off-road, with the Toughness stat affecting the speed loss
  * To create a prop in a custom track, add a tag called "Debris" to a Model and the game figures out the rest

- The first iteration of the Lobby's remaster has been modeled
  * This version is not final, but complete enough for us to call the update done and begin focusing on more grounded updates in the future
  * It will receive model changes in a later update, but for now we believe that the Lobby is polished enough to use
```

## Small Changes
```md
- Cash/Money has been renamed to Credits

- Refactored how data is stored under the hood because we switched to a faster and more reliable package for loading player data

- New players start the game with 10,000 Credits
  * Players with old data that currently have less than 10,000 Credits will have their Credits reset to 10,000 courtesy of the devs

- Spectating now copies the direct position of the subject's camera one-to-one
  * This includes effects from all camera settings except for FOV and camera shake

- Kart Shuffle has been replaced by a new button in the Owned Karts menu that selects a random kart that you own every time you click it

- Transforms now have visual models that replace the wheels when entering different transform modes

- The Waste Wagon is now a secret kart

- Explosions have new visual effects
```

## Balance Changes
```md
- The kart now steers more sharply when under the effects of the Power Orb to match its speed boost

- Slightly adjusted the stats of every vehicle to no longer use decimals inside of their stats to improve readability

- Removed the Drift stat from the game entirely. All of its effects except for boost buildup have been transferred to the Handling Stat
  * The stats of all karts have been adjusted to convert karts that specialized in Drift into karts that specialize in Handling
  * Boost buildup rate has been transferred to the Boost stat instead
  * Handling was retooled to solely be a stat for how easy the vehicle is to control because drag race specialists were unfairly nerfed by the Drift stat impacting the boost buildup. This change intends to allow dragsters to compete for the spotlight once again

- The Off-Road stat has been renamed to the Toughness stat because it now affects your weight in collisions
  * The higher your toughness, the better traction you have and the heavier your kart is (only affects collisions)

- The Boost stat no longer increases the duration of a drift boost, which now have a fixed duration for each tier

- Item Box respawn time decreased from 2.5 seconds -> 1 second

- Boosts no longer use their own formula depending on the boost tier, and now add a flat amount of speed to the kart when active
  * Any combination of boost tiers can be active at once if you're able to chain your boosts in such a way
  * Boosts have their speed addition cut by a factor of 2 for each stronger boost that is active

- Stun time from explosions decreased from 4 seconds -> 2.5 seconds

- Sun time from tumbling decreased from 2 seconds -> 1.25 seconds

- Wormhole has been completely recoded. Instead of teleporting you immediately to your destination, it will follow the path of the track at a speed of 250 studs/sec over a short duration
  * Max amount of Wormholes at once: 1 -> 2
  * Let's be real, immediately teleporting is kinda unfair
  * It will still drop you off early if you end up taking the lead
  * You are completely intangible during the item's duration: you won't collide with items, item boxes, or other drivers

- Gatling Gun & Wrecking Ball proved to be a bit too chaotic during testing. We believe that the items themselves are fine, but the distribution needed to be slightly tweaked
  * Max amount of Gatling Guns at once: 2 -> 1
  * Gatling Gun global cooldown: None -> 10s
  * Max amount of Wrecking Balls at once: ∞ -> 1
  * Wrecking Ball global cooldown: None -> 10s

- Item sets on all tracks in the base pool to contain more items per set, preventing players from unfairly missing items they should have gotten

- Respawn time decreased: 3.5s -> 2s

- Increased the radius of all explosions by 5 studs
```

## Bug Fixes
```md
- Fixed an oversight that caused extreme lag when using the Gatling Gun on tracks with a lot of parts

- Drift boosts of two different tiers no longer overwrite each other
```
## [Enjoy and play here!](https://www.roblox.com/games/9416437817/Karting-League)
