Information about this mod
- Description
- Fix Perk Deck Description
- Tweaking this mod

### Description ###
-------------------------------------------------- 1
Your armor no longer regenerates.

Your health is reduced to 1.

Upon dieing you will enter Swan Song.
You gain 6 seconds of Swan Song duration.
(Stacks with Swan Song skill)

Your movement speed is increasd by 30% during Swan Song.

-------------------------------------------------- 3
Damaging enemies increases Swan Song duration by 0.7 second and additional 0.025 seconds for each armor tier above 2-Piece Suit.
0.5 seconds cooldown

(Swan Song duration can not increase above your maximum Swan Song duration. Each time you go down gained Swan Song duration reduced by 1%)

-------------------------------------------------- 5
You gain ##45%## chance to automatically revive during bleedout.

-------------------------------------------------- 7
Killing enemies increases Swan Song duration by 0.5 seconds.
1 second cooldown

(Swan Song duration can not increase above your maximum Swan Song duration. Each time you go down gained Swan Song duration reduced by 1%)

-------------------------------------------------- 9
You gain additional 4 lives before going in custody.

### Fix Perk Deck Description ###
- If you have other costum perk decks, this perk deck might have the wrong description
- To fix this open loc/loc_EN.lua
- In line 1: Change the default number 22 to the position this perk deck is in game.
-- There are 21 official perk decks at current time
-- Or you can just count from the top to the position of this perk deck

### Tweaking this mod ###
!!!Open the *.lua files with a text editor. For example window's default editor (not recommended). Highly recommended: Notepad++ or Visual Studio Code to get a cleaner representation of the code.

Outline on the files:
-### loc_EN.lua ###>>> localization and in game text description of perk deck

-### player.lua ###>>> contains the logic to make the perks work.
Edit this only to do major changes or change the percentual decrease of gained Swan Song time


-### skilltree.lua ###>>> contains the player upgrades of each tier of the perk deck; perk deck costs editable (pdc1-pdc9)
If you want to remove the no-armor-regen you can comment out line 21:

"berserker_armor",

to

--"berserker_armor",

. Same applies for other player upgrades. Make sure to seperate player upgrades with a comma and don't have a comm after the last player upgrade.

-### upgrades.lua ###>>> contains the numbers to tweak at; necessary documentation in the file; variables are sorted like the perk deck description at the top



