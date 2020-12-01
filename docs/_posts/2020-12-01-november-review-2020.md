---
layout: post
title: November Development Review - New Name, Same Game!
description: We got a new name for the game! And item tiering is finally done.
summary: We got a new name for the game! And item tiering is finally done.
---

The biggest news of the month is probably our rename - from now on the game will be known as **TypoTales**! The whole renaming thing took way too long... and with that out of the way - let's focus on the gameplay stuff instead! :)

### Item Tiering
It's finally done! Items now come in various tiers. T0/T1 are the weakest and higher tiers offer stronger stats, effects and skills.
Every player will start with some T0 Novice Gear featuring simple skills. T1 with more choices and skills becomes available at level 5. T2 starts at level 10 and features the set of weapons you've already known and used in the last playtest. Afterwards tiers will advance every 10 levels, So T3 starts at Level 20.

While I'm still working on making this all look and feel good inside the data editor, ingame it is already nice and dandy. Searching for items with /d now displays matching item groups (if there are any) and stuff that isn't assigned to them separately, like this:
<br>![Item Groups in /d]({{ '/assets/images/10/describeWithItemGroups.png' | relative_url }})

Selecting an item group will then show the tiered items assigned to it:
<br>![/d of an Item Group]({{ '/assets/images/10/itemGroupDescription.png' | relative_url }})

### Foraging Rework
Can't just change how items work and leave foraging as it is, right?
Foraging was one of the first things I've ever implemented, and I never touched it afterwards, therefore both the editor and the way it was implemented are old and ugly. I've changed the way how loot is distributed during adventures two times since then and wanted to adjust the way how foraging loot works accordingly.

Here's a screenshot of our old Editor for Harvesting:
<br>![The old foraging loot editor]({{ '/assets/images/10/foragingLootViewBeforeRefactoring.png' | relative_url }})

The aim of this rework is to also allow the selection of entire item tiers (so we don't need to have multiple data entries for Wood T3 and Wood T4 with the same probabilities and all) while also retaining the "old" implementation for untiered items (there might be some in the future, who knows?).

As always, I wouldn't be in the right state of mind if it did not end up with a lot more fluff and features than I originally intended (a big <3 for feature creep, I guess!), so time & weather requirements are now no longer in a dropdown and can be individually enabled & disabled. While at it, I also added another category for very rare items which shouldn't be included in the normal loot calculations. More on those later!
<br>![The new foraging loot editor]({{ '/assets/images/10/foragingLootViewAfterRefactoring.png' | relative_url }})

Back ingame, you can now select the tiers you want to search for - though selecting multiple tiers will yield more items in total, so keeping your eyes open for multiple tiers might be worth it!
<br>![Foraging view with tiers]({{ '/assets/images/10/tieredForagingView.png' | relative_url }})

#### How the new foraging loot distribution works
Earlier every item had a value, and we'd just randomly select an item from the list that'd still fit into the players "gathering budget". This budget would increase linearly with the players foraging level. During the last playtest this... ended up being a bit weird since high level players would end up finding way too many items. 🙃

Now we got rid of this budget thing. Instead, players will just get X items from their loot list. Odds are defined through the weight. X might slightly increase every couple levels, or when the player selects to forage for more than just one item tier.

Afterwards, we roll the dice for the very rare items - those have a fixed probability and are unaffected by the other items in the loot list. Right now there's only one item in that pool and besides maybe event stuff I can't think of many other applications for this category.

### Crafting Bonuses!
Finally, here's another small change: In the past, crafting levels where more of a decoration and had no use - it was about time to improve upon that.

From now on alchemists will receive a chance to craft bonus consumables if their level exceeds a certain threshold, while armor- & weaponsmiths can now craft high-quality gear, which offers small stat improvements. If a player's level is too low they might actually end up with low-quality stuff if they craft it themselves. I somewhat hope that this makes trading and specializing in a certain profession a bit more desirable. Experience values have also been tweaked in order to make leveling up easier.

### Next Steps
The next (alpha-) playtest is not too far away! The game just needs some more finishing touches, mainly more content and balancing as well as a small tutorial. T3 Content (Level 20+) will probably be patched in one or two weeks later, once players get there.

As mentioned earlier, [Patreon Supporters🡕](http://patreon.typotales.com) will get into the game a few days before others. Afterwards, active players from the last playtest will receive access. Going forward, once everything seems stable, I'll let more people into the game by allowing friend invites and handing out more alpha-keys in limited quantities. The Playtest will run until the end of January, after which we'll have a small downtime for the transition into the (more open) Beta Phase. There will be another world-ending event at the end of this playtest, although a bit different from what we had last time.

#### Aaand that's it for now!
As always, stay healthy and see you at the playtest. :)