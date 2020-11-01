---
layout: post
title: October Development Review
description: We are slowly getting closer to the next playtest - let's have a look at what happened behind the dev-curtains during the last month.
summary: We are slowly getting closer to the next playtest - let's have a look at what happened behind the dev-curtains during the last month.
---

A month has passed since the world ended. As such, I had a lot of time to add new features without worrying about how those changes will affect the live environment. Let's have a look at what I did and what's going to happen in November! :)

### Guild Content - Loot & Glory!
First of all, I spent about half of the month creating more guild content.
There will be a new currency for guilds: 🎖️ Glory. In order to achieve it, your guild needs to successfully participate in Campaigns. In the near future it will be used as a special currency for territory upgrades and buildings.
 
Speaking of campaigns, those come in two variants:
- **PvE**: Explorers can now find beast tribe sites which guilds can then attack.
- **PvP**: Guilds can attack (or defend) other guilds in the newly added guild warfare.

In both cases, multiple guilds can band together in order to take out stronger opponents.
I'll probably have to add some limits on guild warfare in the future, so strong guilds won't stomp small or new guilds all the time. There are a couple of options that I'll investigate in the following week.

### AI Improvements
I significantly improved the way the AI interacts with Status Effects - especially if a skill has status effect interactions, such as Backstab or Shed. Skills can now change in priority depending on the existence and count of certain effects... or lack thereof in the case of buffs.

### Rate Limits & Scaling
Let's be honest - Telegram's hardly documented rate limits might be the bots' downfall if it ever gets too popular. Therefore, I spent a couple more days doing research and made some preparations to ensure the game bot won't end up globally muted for half an hour. If that ever ends up happening I got a pretty solid plan B ready to ensure this will only ever happen once. More on that once I push the associated button. 🙃

### Alpha Keys & Friend Referrals
Finally, I've implemented a way to generate alpha keys, which will be needed in order to participate in the following playtest. This way I can fully control how many people can play the game - no more secret command that allows access. Later on the same system will be used for friend referrals - I haven't figured out any rewards yet, but existing players can generate keys for their friends... and the game keeps track of who invited whom. Initially those will be limited of course, and [Patreon Supporters🡕](https://www.patreon.com/Chatventure) will be able to send out more at first. *(Consider this a friendly reminder of its existence. :P)*

### Item Tiering
While not implemented yet, I finished designing item tiering and will start implementing it next week. This and new content will probably take up half of November - the next playtest will probably feature adventure & item content for levels 1 to 30, so there will be at least three different tiers.

### Real Life Launch Preparations
Given that we are based in the EU I'll probably have to include some GDPR (Data privacy) information stuff into the game, and since Patreon basically counts as an income (even if it's technically just donations that barely cover server costs) I'll also have to set up some sort of company before the game properly launches. All this legalese is giving me headaches, I just want to create a game and give people the option to support me whilst doing so... D: 

Buuut complaining doesn't help, so I'll have some business related meetings during this month before we launch into the next playtest. Yikes. Here. We. Go!

#### Aaaand that's it!
Hope all of you had a nice halloween (if you celebrate that) despite the global circumstances and stay healthy.

I think I'll make these "review blog posts" a monthly thing, as it's a nice way to keep track of what I've done & achieved while giving away some insights into the development process. So see you next month! :)