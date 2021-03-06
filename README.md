## Getting Started

Welcome to the VS Code Java world. Here is a guideline to help you get started to write Java code in Visual Studio Code.

## Folder Structure

The workspace contains two folders by default, where:

- `src`: the folder to maintain sources
- `lib`: the folder to maintain dependencies

Meanwhile, the compiled output files will be generated in the `bin` folder by default.

> If you want to customize the folder structure, open `.vscode/settings.json` and update the related settings there.

## Dependency Management

The `JAVA PROJECTS` view allows you to manage your dependencies. More details can be found [here](https://github.com/microsoft/vscode-java-dependency#manage-dependencies).

### Notes
SLARDCRAFT PHILOSOPHY: SLOWER AND HARDER, STREAMLINED FASTER PROGRESSION TO MAX, MORE EXPERIENCE OF UNCOMMON MINECRAFT TECHNIQUES, UNLOCK OTHER WAYS OF PLAYING MINECRAFT, Synergy with forevercraft of on demand minecraft
Marriage of technical minecraft and aesthetics. Deemphasize power gain. Incentivize collaboration. Never so powerful to be invincible to mobs, always partially threatened by mobs, a low cap to power. 
Power is transient in SlardCraft. Power gains through potions, armor, blocks, enchants and food are marginal, slight and small improvements from base.

ADDED:
TESTED:
- Iron Golem farming is removed. Player placed iron golems still drop iron.
- Gamerule for 50% sleep required to progress night, Gamerule for disabling announcements for achievements, Gamerule for disabling elytra movement check
- Diamond and netherite tools and armor are uncraftable. Also removed elytra
-Armor, weapons, shield, bows and crossbows enchanting from enchantment table and anvil is removed for tiers above wood and leather. enchanting for shears and fishing is still available.
-Villager trades are sanitized for enchanted armors and tools as well as restricted tiers.
-Mob drops will also be sanitized of enchantments before dropping unless wood or leather. 
-sanitze player pickup event as well
-Sanitize chest drops to convert all enchanted armor and tools to unenchanted variants. Also sanitize diamond and above to iron. Caveat, unless wood or leather.
-big and mega diamond custom items
-chat color for MEGA DIAMOND
-piglins dropping swords is fine, bc it has to be cooked to yield one nugget. zombie piglins on the other hand drop nuggets and ingots on kill by player. can reintroduce some farming mechanism later, but for now just remove it.
-sanitize pigling barters
-only sanitize entity item pick up on player pickup, should be fine for foxes
-nerf beef and pork, - when PlayerItemConsumeEvent get player in field. manually change hunger to proper value
-steak and pork 6 hunger8saturation
-add seasoned variants that bring it up to slightly better than normal. Made with gold nuggets
-seasoned steak and pork - 8 hunger 13 saturation
-remove ability to rename big,mega ore and seasoned meats. they rely on checking if the item meta data is the same for the crafting and eating properties
-New Recipe for custom sugar. Used for haste potion and haste cookie. made of 1diamond and 3 sugar to yield 4 fancy sugar.
-New Recipe for fancy cookie. Uses custom sugar to give 22.5s of haste1 for 1 cookie. recipe gives 8 cookies
-the new diamond pickaxe can maintain the durability of the iron pickaxe inside of it's metadata
-Diamond coated iron pickaxe in smithing table, created in upgrade thing with a new iron pickaxe. 10 durability diamond pickaxe, drops iron pickaxe on breaking. Maybe try to preserve iron durability before and after diamond coating wears
-Remove sanitization for coated pickaxes. 
-Gotta set destory item event for coated pickaxe
-remove repair diamond pick axe....
-bound world size to 3kx3k
-init.slard instead of play. and play is the ip.

UNTESTED:
-nerf trident actually. maybe only allow riptide

TODO:

-wiki with patch notes
--Upload the wiki
--how to play, and images of recipes still not in
-test piglin farming. behaves the same as zombified piglin. arg for keeping it in: only yields max of 8 ingots per hour, considering looting 3 and killing efficiently. Cons - mining yields about 8 ingots per hour, 10~ ingots per hour with big. So farming piglins is a viable way to get gold which is really boring. So im incentivizing a really boring way of playing. solution, make mining gold more available by increasing map size...? Ban gold farming from pigs. - more viable in the beginning can readd later.
-remove mending

-add silk touch 1 to coated pickaxe


NEVERMINDS:
-Sleep fatigue can stay.
-Monsters shouldn't drop enchanted bows or crossbows.
-No extra suspicious stew, not worth the hassle for such a early game item.


V1.1 Polish existing features And Add currencyness:
-wiki with patch notes
-Elytra Rental. one diamond = 1 minute of elytra.
-INIT.minecraft.jacobyng.com Currently, even viewing available minecraft servers will start it up. so when dealing with multiple it will always initiate the other servers... Have play. be the main one. Ask people to use play and initialize server in their web browser with init
--Rather than init minecraft. Should use API gateway and a web interface.
-gamemode creative don't sanitize pickups
-make a nice sound on big and mega finds. make a nice sound on mega and big breakdowns. Add additional exp gain on breakdowns
-Allow iron farms. just have to kill the golem for iron.
-Allow some sort of piglin farm. Has to be heavily nerfed, and player involved like player kill. Maybe make a micro gold grain?
-hero of the village sound for all players when a mega diamond is mined.
-breakdown anvil sound when crafting broken diamond and ore. also grants exp.
-New bong water potion. brew grass or tall grass, all variants including lingering for hotboxing, for potion of nausea
-New potion of haste with all of the variants. Follow timings for other potions.
--For now may be easier to modify speed potion with fancy sugar in crafting table. kind of sucks but it is what it is. We can just make the haste 1/2 and long variant for solo use.
--or possibly cookies are good enough? might make potions a 1.1 feature
-readd repair of vanilla and legal items in anvil

BUGS:
-BIG,MEGA ORE NEEDS to replace furnace recipe.

v1.2 New PVP features
-Duel mode. Wager a bet. Tax one diamond. Don't lose inv on death. Respawn on point of death.
-firecharge shoot ghastprojectile doesn't blow up dirt but explodes with AOE damage
-Challenge "For better or for worse". Cost one diamond. Buff keep inv on death. Debuff Can't wear armor. Debuff marked for bounty of one diamond. Stays on until death.
-Challenge "For better or for worse", can gain access to location of others doing challenge.
-Challenge "Diplomat", cost 3 diamond. Bounty of 3 diamond and gold in inventory. Buff keep inv on death. Can only wear golden helmet. Gains one gold ingot per every 10 gold ingots in inventory per day. Location available to everybody. Choose lowest amount of gold in inventory that day as interest amount, incentivize keeping gold in inventory
-Diplomat caveats rolling window of 20 minutes, clock only goes when another player is in the server 
-scoreboard always see diplomats gold and anyone else who has a bounty and their bounty
-diplomat rate of interest is faster the closer you are to 0:0


Thoughts:
-Running tally of turned in diamonds. Each turned in diamond yields x11gold
-Can convert 20g to 1d
-evil diamond?
-potion cooldown system?
-consider bounding the world 10,000 radius and pre-rendering the world
-Sanitize itemMeta as well, not just enchantments?
-Is it possible to make item stack bigger?