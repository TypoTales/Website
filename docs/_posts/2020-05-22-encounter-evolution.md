---
layout: post
title: Encounter Evolution
description: When players go on an adventure, they have to fight multiple waves of enemies. Each of those waves is internally called an encounter, and this blog post takes a look at how this encounter system has changed over time.
summary: The Encounter system has grown quite a lot since alpha!
---

When players go on an adventure, they have to fight multiple waves of enemies. Each of those waves is internally called an encounter, and this blog post takes a look at how this encounter system has changed over time.

![Your usual encounter after starting an adventure]({{ '/assets/images/encounterEvolution1.png' | relative_url }})

#### A brief history~
As with most things during the alpha, the very first iteration was as simple as it could be - as soon as a player starts an adventure, all encounters and monsters would be generated at once and then just served one after another.

This worked nice, but had a tiny performance problem: if an adventure was abandoned (or the player died), a lot of the generated encounters would just be scrapped without ever being used. As the need for longer / harder adventures grew, this didn't seem to scale well. It also wasn't very flexible as the "path" a player would take was predetermined.

Changing the system to generate new encounters on the fly after the previous one was finished was rather easy and already implemented back when the second Gobline Cave launched, but there was still a lot to come...

#### Enter: Scripted Encounters
The new encounter system is a lot more complicated than just the good old "spawn enemies, enter battle"-approach. Each adventure can now spawn special encounters, containing specific monsters, dialogue, and even branching paths with multiple choice options leading to both traps and loot. They can spawn both at random and at set waves, so in theory we could now have stories where an adventure purely consists of only one huge scripted encounter chain and a multi-stage boss fight at the end - no promises though, I'm kinda lacking the creativity to come up with those.

![Oooh, shiny!]({{ '/assets/images/encounterEvolution2.png' | relative_url }})

Item loot works different than in most other games: every player in the party will get the full loot, as that's easiest to implement and avoids arguments about who should get what. The game shall be just as enjoyable with friends as it is supposed to be alone after all.

Also, while we are speaking of loot - you'll now lose all your loot if you abandon your adventure or the whole party dies. So, if having a very rare item in your backpack or one of your previous actions attracts some strong monsters, you'd better fight for your life~

![Obviously those numbers might need a bit more tweaking]({{ '/assets/images/encounterEvolution3.png' | relative_url }})

If none of those fancy scripted encounters is chosen, a random battle is instead generated the old way, though even those might now randomly get spiced up by surprise attacks and other nasty (or helpful) stuff, like enemies with random status effects. 

Aaand that's it, basically. I'm still working on getting the data editor to display all the configurable stuff in a proper manner (its a looooot) - slowly reaching the point where all that's left missing is proper content for all the systems I've been building. :)