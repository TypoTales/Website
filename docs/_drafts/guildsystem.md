---
layout: post
title: Design Talk: Guild Territories
description: Let's talk about guild content this week!
summary: Let's talk about guild content this week!
---

Let's talk about guild content this week!

Every guild can purchase its own territory - those territories are spread out across the country, and are the exact reason why the country itself doesn't get attacked by armies of monsters: Guild Territories serve as a perfect first line of defense against unwanted intruders, and guilds usually are capable of defending themselves pretty well.

After a guild has gained control over its plot of land, it can start constructing buildings in whatever way its members see fit, and each player has to decide on an action they want to do for their guild every day... 
There are three options, and if you've played ChatWars in the past, you might already know how parts of this will work:

##### 1. Defend
Once you start exploiting the land and constructing buildings, there will be attacks from monsters at night - the adventurers and their companions will have to band together to defend their turf in order to prevent looting and destruction. 

##### 2. Scout
Search the surrounding areas for monster hideouts or other points of interests. This might unlock new adventures for your guild or special campaigns for the following day.

##### 3. Join Campaigns
Join the offensive on a previously scouted campaign for a chance of loot and glory. Multiple guilds can band together to take down especially strong ones. The individual guild leads will have the final say on which campaign their guild should take, so keep in mind that they might actually betray you - thus leaving you without reinforcements in front of that mighty dragons' cave.

### Guild ranks
Joining a successful campaign as well as defending your territory from an attack will cause your guild to receive glory, while failing those will cause you to lose some. The higher your rank, the more unwanted attention from monsters and bandits you'll get, but at the same time, your scouts might find more valuable targets...

### Guild PvP
While not encouraged by the countrymen for obvious reasons, it might also be possible to raise campaigns against other guilds at some point in the future.

## Territory Buildings
Now let's take a look at the buildings you can construct on your territory and what they'll do for you - you might not be able to build all of them.

#### Watchtower
The watchtower is a central peace of every guild territory - it allows you to scan the surroundings for incoming attacks, so you can muster your defenses accordingly. Higher levels increase the accuracy at which the strength incoming attacks are estimated.

#### Warehouse
Shared Guild Storage space will be limited by the warehouse level. Upon building one, the commands /store and /collect will become available to guild members in order to access it.

#### Training Ground
Players can leave their companions at the guild's training ground so they can gain levels by sparring with each other. Higher levels increase capacity and experience gains. 

#### Guardhouse
Players can leave their companions at the guardhouse as a stand-in defense against incoming attacks. Higher levels increase capacity.

#### Farms, Mines, Lumberyards
Those will automatically produce materials usually found during gathering trips and adventures. Higher levels increase the amount and quality of items. Produce will be automatically stored in the warehouse.

#### Walls
If you build walls around your territory, you'll receive defensive bonuses when you are attacked. Those will also be the first thing getting damaged or destroyed if an attack isn't stopped, so keeping them in a good shape should be a priority.

### The Guild Bot
There will be a new Bot helping you to manage your guild. Every Guild will be required to have a group chat with the guild bot inside, for a very simple reason: Every day, the bot will post a poll where players can select their individual action, so everybody else can immediately see what the others will be up to.

## Insights: How it came to this

Originally, I wanted each guild to have it's own spot on the world map and compete for actual territory, but given the text-based nature of the game and varying limitations through telegram, that just doesn't work out properly.

#### Plot twist: Working on different Platforms is hard, even if you just write a Telegram bot and everything is text based.

The initial plan was to give each guild their own, small map, where they could place buildings and such on a grid - but rendering it in a way so that it's displayed in an acceptable way on every device is hard.

There's so-called `monospace text`, where every letter is supposed to have the same width. Sooo... creating something that resembles a proper grid on each device should work, right? 

Wrong.

Even grid characters such as `┌ – | ┬ ┼` tend to not line up properly. Once you throw Emoji into the mix, Android and Apple (let's not even mention desktop clients) seem to render stuff completely differently. Also, given that every device has a different screen width, resolution and font size, this might end up looking super ugly with line wraps in the middle of the map.

[Screenshot]
Left: iOS, Right: Android

An alternative to a text-based representation of the map would have been to render it as a png and send the image to the players - but that would consume way more server resources, as well as draining a potential low data bandwidth.

So, I've decided to scrap the map-idea entirely. Let's take a look at what's left.

## Guild Territories: Simplified


<br><br>
That's all the plans on guilds for now - I'm open to feedback, so come discuss it in the Group Chat!