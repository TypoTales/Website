---
layout: post
title: January Development Review – new content when?
description: A look back at the first month of 2021, and some irl stuff.
summary: A look back at the first month of 2021, and some irl stuff.
---

### Playtest Stats!
![Playtest stats!]({{ '/assets/images/13/20210201_stats.png' | relative_url }})
While we cracked more than 100 active players within 24 hours in the middle of the month, now we are slowly losing a bit of steam, which is understandable – the lack of new content kinda spoils the fun for people who are past level 15. It kinda fits into my expectations to be honest, which is why I originally planned for the world to end around now. Whelp, can't help it, though foreshadowing for the impending doom (end of the playtest) will soon start. Players who participated in the previous playtest might know what this means and already look forward to meeting a certain character again. 🙃

### Fixing the Economy: Resource Sinks!
Most people have begun piling up a huge amount of certain materials, and I've been slowly adding ways to spend those – starting with higher possible upgrade levels with increasingly insane material costs and adding a Gem cost to `/powerup`. Yes, it's possible to upgrade Items past +5, but you won't necessarily need that to advance through the content... it's mainly just for people who want to show off.

Furthermore, Upgraded Weapons become soulbound and can no longer be traded – this way new players won't just receive a free Legendary+10 Weapon/Armor and actually need to spend resources to upgrade their stuff. Being unable to trade those things is a bit annoying, but it saves the economy and also makes the market a bit less convoluted!

This still leaves us with Stones, which will soon be craftable into siege ammunition for the upcoming siege weaponry. Wood, Metal and more Stones will be used by the upcoming Effigy. Alpha Keys will also become craftable, though the recipe will be very expensive and use up yet unavailable resources.

### Speaking of guild content...!
Last week I posted a summary of the upcoming guild content aaaand I already got something to add!
Turns out that the current way how loot is distributed on shared campaigns may be a bit... frustrating for smaller guilds. I think this is best explained with an example:

Let's say we have two guilds, A and B.
- A has a Campaign strength of 90,
- B only has a strength of 10 but found/owns the Campaign site.

##### (1) Participation Share (Current System)
Right now it's split up between the participants depending on their participation, meaning if a ra re item is found, A has a 90% chance to get it and B has a 10% to snatch it.

This is especially unfair when B originally found the site, so here's the new loot mode to fix that:

##### (2) Round Robin
Items will be equally distributed among all participants, starting with the campaign site owner. So if 3 Items are found, B will get two, A will get one. If you are familiar with other MMOs, this should sound pretty familiar to you.

The owner guild of a campaign site can set their preferred loot mode for the campaign before sharing it. I'm still debating with myself on whether this should also split guild fame evenly, as that could be exploited to boost weaker guilds.

### T3 Equipment
I originally intended to add some skill changes into the new equipment tiers, but for now it will just be increased stats, so we can finally slay monsters on level 20+ Missions.
Stat growth in itself has been bothering me quite a lot, because the lack of stats per level make balancing a little harder than I originally intended.

Let's say T3 content starts at 20 and ends at 30.
Right now I assume a player starts at level 20 with T3+0 Equipment.
Level 20 Adventures should be manageable without upgrades, while Level 29 Adventures should be manageable with some quality gear that's +5. Higher upgrade levels will obviously make things easier.

<br>![Tier Editor]({{ '/assets/images/13/data_editor_tiers.jpg' | relative_url }})
I added a neat little overview into the data editor which helps keeping track of equipment stats in between tiers, which will help add and adjust new tiers in the future. Especially immediately knowing how the Stats at +5 will look like is a great help.

I still haven't finished prioritizing this week's tasks on the roadmap, but it's likely that not everything will make it in, including T3. 

### An IRL Update
*Let's share some real life stuff in here for once!*

I didn't really get to add much content over the past two weeks for a simple reason – I randomly found out that the german games awards have a category for newcomer prototypes and couldn't resist trying my luck there, so I spent some (okay, maybe way too much) time assembling a good-looking PDF file explaining what the game is about and polished certain aspects of the early game experience. I don't really expect to win anything, as the game's text-based nature is pretty... abstract after all, but one can still try, hope and dream. :)

Furthermore, I applied for this year's online version of the [Game Mixer](https://www.goethe.de/ins/za/en/kul/gen/gnt.html) program and got accepted into it! It's an international program where about 20 people from all over the world join together to build games within two months, organized by the Goethe Institute. This will be a bit like a part-time job for me until April and I'm super excited to see how it unfolds. ^~^

...This shouldn't interfere too much with my work on TypoTales, instead I'm hoping to collect some new inspiration through it. Aaand to be honest, working on a game that has some real-time interactions and actual graphics will be a really nice change for once, after a year of mainly working with consoles, backends and automated tests... :D

<br><br>
That's it for this month – thanks for stopping by, I hope you'll enjoy the upcoming changes to the game! :)