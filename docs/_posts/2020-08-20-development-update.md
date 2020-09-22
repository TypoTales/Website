---
layout: post
title: Development Update
description: It's been some time since the last blog post... and quite a lot of things happened since then.
summary: It's been some time since the last blog post... and quite a lot of things happened since then.
---

It's been some time since the last blog post... and quite a lot of things happened since then, besides me literally melting away from the relentless summer heat.
Let's dive right into what I've been working on over the past two months!

### Mercenaries
More or less randomly generated Mercenaries will now occasionally frequent the local tavern, eager to be permanently hired by players for some of their hard earned money. Their price will decrease as they wait, but once one player hires them, they'll be gone for everyone, until eventually a new one shows up after a set amount of time.
There are still a lot of ideas to expand on this feature in the future, but for now, it works and that's what matters most.

![A mercenary ready to be hired ingame]({{ '/assets/images/7/mercenaryIngame.png' | relative_url }}) 

And this is how they look within the editor:
![The Data Editor for mercenaries]({{ '/assets/images/7/mercenaryEditor.png' | relative_url }})

### Money
Right when I wanted to test those mercenaries, I noticed that there where no options to receive gold yet. Whoopsie! So yeah, gold can now be looted from certain monsters and awarded for clearing specific encounters and adventures. All gold values you might see in this post are subject to change.

### Monster AI
I've vastly improved the AI of Monsters & Companions - which in itself wasn't too hard, given that before this change every attack/target was chosen completely at random.

Instead, now every skill can define its own target preferences, which will in turn be used to prioritize what skill to use and on which target. No more healing people at full life and such! Additionally, there's now an option for monsters to only use skills under certain conditions, like having more or less than x% HP or while affected by a certain status effect. Multi-Phase boss fights, anyone? :)

All in all, I hope that both your companions and your enemies will appear somewhat smart in the future. But please don't quote me on that since I've also added a threat system for the latter.

### Data Editor
With every new feature I'm implementing into the game, there's probably something that needs to be changed in the data editor as well, so it has grown a lot - to a point where I sometimes wonder if I spend too much time on polishing it. But then I have to admit that the ease of use and (at least some) convenience features really pay off when adding new content! Take the recently added loot summary on the right side of the adventure editor for example:

![The Data Editor for Adventures]({{ '/assets/images/7/adventureEditor.png' | relative_url }})

### Guild Features
I've finalized the design process about how guild territories and all should work and even drafted a blog post about it - and then totally forgot publishing it, hehe. While I'm going to post it soon, I'm still debating with myself whether I should add the barebone stuff before launching into an open beta or not.

### Game Content
Finally, this week I've been working a lot on adding more content into the game. Some Adventures and a multitude of random encounters. Treasures and Mimics, branching paths, traps and surprise attacks... all kind of things. It takes some time to come up with those, but once they are here, they can be reused for all kind of adventures where they fit.

![The Data Editor for Encounters]({{ '/assets/images/7/encounterEditor.png' | relative_url }})

Next up would be the dreaded act of balancing, given that stuff right now is either too easy (oneshot) or too hard (also oneshot...). I want the selected player race to matter stat-wise, even if its just in the early game, though that makes some race/weapon combinations tricky to deal with.

### The Beta Launch aka when will the Servers go online
I hate not being able to give accurate estimates over and over, so I'll just stick with saying soon(tm) for now.

I'd mainly blame my hopeless perfectionism for that: there's just so many things I'm still not 100% comfortable with and still want to improve upon, as well as the general lack of content that I'm currently getting rid off.

Oh, and there will be a small playtest next week.

Well, that's it for this post. Hope you enjoyed the read!