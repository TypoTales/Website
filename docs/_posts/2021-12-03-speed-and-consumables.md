---
layout: post
title: Design Discussion – Speed and Consumable Changes
description: A first glimpse on what's going to change before the open beta starts.
summary: A first glimpse on what's going to change before the open beta starts.
---

Now that there's the [@TypoTalesDevDiary](https://t.me/TypoTalesDevDiary) Channel on Telegram, let's change up the format of these blog posts a little. Instead of going into detail on what I did and didn't do, let's discuss game design!

So, recently we had two discussions coming up in the Community Chat: One about consumables, and one about speed. Let's dive into those and then present you my solution to each problem.

## Let's talk about Consumables
Consumables have one big issue right now: nobody's using them! Or, well, most of them.
Within the last month, within battles about 2400 Health Potions and 1050 Mana Potions where used. Next up would be 470 Bombs and 320 Berserk Potions. Anything else? Not so much. The situation is the same with rest actions, but here people tend to use lower tier potions more often.

It seems like in most situations, it's just not worth spending an entire turn for an item, so anything besides the occasional emergency hp/mp heal feels like a waste of an action.

### Upcoming consumable changes
It's fairly simple: Using consumables will no longer count as a turn action! Instead, you will be able to use one of them right before selecting your action, and the effect will activate before all other actions are processed for that turn. There will also be some tweaks to consumable effects and durations.

Additionally, Items will now have a cooldown of X turns before they can be used again, depending on the strength of the consumable and some other factors. Further down the road, I'll add special equipment aimed at frequent item users, which will feature cooldown reductions, increased item efficiency and additional adventure backpack slots. Maybe we'll even see some builds focusing entirely on using consumables that way?

Which brings me to the other design headache:

## The issue with speed
Speed in turn-based games is a weird stat. As long as nobody dies or gets impaired by some status effects within the same turn, the turn-order itself doesn't really matter, so it's usefulness is heavily situational. Adding some secondary effect to the stat would certainly help make it more valuable.

### Looking at other games
Let's take a look at some popular games out their and how they are handling speed stats, then think about how these solutions might work within our game.

#### Pokemon
Pokemon follows the same implementation we do right now: Speed just affects your turn order. Back in Gen1, it also affected crit chances, but they quickly got rid of that with the following generations. *Nowadays, when looking at the speed stat for competitive builds, they only revolve around the question of how much speed is necessary in order to outspeed a certain other Pokemon.*

#### Temtem
Temtem is a pokemon-like MMO which focuses a bit more on competitive gameplay. Their take on speed is that skills have different priorities, and these act as multipliers for the speed stat when determining turn order. *In TypoTales terms, with this system, having increased Initiative would not automagically mean that you'd move first as it would only act as multiplier on your speed stat. It's interesting, but since TypoTales has less of a competitive character to it, I feel like it would only overcomplicate things a bit.*

#### Final Fantasy
The FF series iterated a lot on its battle system over the years, so this is a real honeypot when it comes to research for turn-based battle systems and how they evolved.

In the first two Final Fantasy games, the speed (or agility) stat also determined hit & evasion chances. *I don't really like hit & miss chances and want to avoid implementing them, so their solution won't be directly applicable to our dilemma here. Technically we could translate it so that the difference in speed stats between target & attacker affects the defense rating in some way – like, if you are fast enough, you can manage to pierce your enemy's defenses for some reason.*

In FF3 it affected how many hits characters would land when executing physical attacks – now that's more interesting! *Since every attack is a skill and there's barely a default "normal attack", translated to TypoTales, this could mean that you get a chance to select two (or more) skills depending on your speed stat. In the end, this would probably feel very clunky and end up in way too many skills per turn in later levels. Alternatively, some skills could also get a speed scaling in their damage calculation.*

Afterwards, they moved to the ATB-System, where combatants had an action bar during battle that'd fill faster depending on speed. Only once the bar is full you'd be allowed to select an action, so they basically got rid of "strict" turn-based combat altogether. *This is a really nice solution to the problem, but hard to execute properly in a text-based manner, especially with Telegram's API limitations. Imagine someone playing a super-slow build and having to wait for others to make like 10 actions before it's their turn, that'd be a looot of text at once - and what should happen if a player dies? Also, multiplayer parties would be more complicated as everyone would be prompted to select a skill at different times.*

### Now, let's fix speed!
Right now, having specific skills receive damage bonuses depending on their user's speed seems easiest to implement, without reworking the whole battle system in itself. Obvious contenders at first would be the Longsword and all Bows, as well as some monster skills. Maybe later on we'll have a separate weapon type fully focused on speed, like claws, daggers or knuckles.

### Two problems, one solution?
So, we now got consumable cooldowns, right? What if speed could also affect those? If a player is faster, they could use items more often! Players wanting to focus more on throwing items at their teammates (and enemies!) could specialize into speed.

*None of the things mentioned here are set in stone yet, so things might further change before they are implemented. Let me hear your thoughts and ideas, so we can make this game as best as possible! :)*

## What's next?
With the playtest ending this month, buckle up for a series of story adventures leading up to the end of the world! Everyone who finishes these will receive a special title to display on their profile in the upcoming open beta, which will launch February or March 2022 and will have no more access restrictions. And if everything runs smoothly, there won't even be any more resets!