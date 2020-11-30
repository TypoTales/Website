---
layout: post
title: A small postmortem and a glimmer of light 
description: The land is shrouded in darkness. Let's have a look at what happened and what will happen in the future in our very first developer blog post!
summary: It is alive!
---

The land is shrouded in darkness. Let's have a look at what happened and what will happen in the future in our very first (and probably way too long) developer blog post!

#### A look back
Development on the game originally started in November 2018, although back then it was just a plaything for myself as I tried to get back into SQL for some Database Development, hoping I could use that in a new project at work. Out of curiosity on how a different game on Telegram works, I tried hooking up the application to a Telegram Bot and since then it slowly started to look more and more like a "game".

It was a fun time, with a tiny hand full of people the pre-alpha started already a month later in late December, while adding in more of the features you'd usually expect from a "proper MMO", such as Parties, Guilds... up to the final Update on April's Fools day, titled ChatventureMon, which added a way to capture monsters in battle and force them to fight in a party along the player. That was in an attempt to make Single-Player Gameplay more worthwhile, which - even though this is technically an MMO - felt and still feels very needed.

That was the time where development started to break apart. The ever growing pile of ideas grew more and more and I've failed to properly prioritize what to do - heck, I didn't even have a proper idea on how the world should look like, which was the main reason why there where still only placeholder items in the game. 

So, almost a year ago, I've stopped working on Chatventure. I've tried getting back into it multiple times, but never properly succeeded at doing so. Not knowing where to start since there where so many things left to do, I instead ended up only adding to the pile of half-way implemented features every time, which didn't help in the slightest. Feature Creep got me. Hard.

#### Darkness covers the land
Finally, in January 2020, I've ran out of free credits at my cloud hosting provider (rip free offers for being an IT student), which made me decide to finally pull the plug and post the announcement that CV would be dead. The huge pile of paper sheets with ideas and plans for the game which has been resting right next to my computer monitor for the entire time went into the paper bin directly after posting it, which felt awkwardly liberating.

#### The Glimmer of Hope amidst the darkness
Which brings us to early March - thanks to the ongoing Sars-CoV-2 pandemic I had to cancel my plans of travelling the world and instead got stuck at home. Yay.

Trying to do the best out of the situation, I decided that it'd be sad if people just messaged the good old ChatventureBot and didn't get any response at all, so I set up a small ping-pong bot that just responds with the same message to anyone. Which got me thinking and made me start doing more cleanup work. Heck, now that I can look back at it, code quality really began to suffer from the ever increasing amount of features. Ended up deleting 49 Files just in the first week - back then every skill had its own class, which worked well during initial development, but doesn't anymore once you want to add fitting skills for each monster and such. Now it's just a one class fits all approach, with exceptions for things that require special logic.

Speaking of adding new Monsters, Skills, Status Effects and all those things - in the past, that was all done through a huge Google Sheet with a separate table for each type of object.


![Skills in the Data Table]({{ '/assets/images/skillDataTable.png' | relative_url }})

This worked like a charm, but whenever adding new stuff, more columns have to be added, making the whole thing... grow pretty wide. So in order to get rid of that, I began creating a special application for creating and editing ingame data.

![Skills in the Data Editor]({{ '/assets/images/skillDataEditor.png' | relative_url }})
(That's the same Table from before, just neatly organized in our cute little data editor)

I'll probably finish the application by sunday, then it will be one or two days to make Chatventure work with the new data format, since I've been making some small optimizations here and there. Afterwards, the cleanup continues, while I try to take a more structured approach than last time and being more open about what's happening in the background (which is the main reason why I've started this blog).

#### A look into the future
I'm still not 100% sure on what I should work after that, but it's going to be either finishing the ingame market or scripted encounters. Anyone remembering the Screenshot I've once posted containing a treasure chest? Yeah, that was one of those scripted encounters. I hope they'll end up adding more variety to the samey adventures we've had in the past as they allow for random things to happen. I'll probably go into more detail about them in a future post. There's also some new Telegram Bot API features I want to check out and play around with, maybe there's something which can be of use for us. :)


Aaaand that's it for today! As always, please tell me if you like or dislike this format, and what I could improve. See you next time! o/