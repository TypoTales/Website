---
layout: post
title: September Development Review – Power Nodes!
description: Power nodes are coming soon™. Here are some more insights on what to expect.
summary: Power nodes are coming soon™. Here are some more insights on what to expect.
---

This month's blog post had been a bit delayed since I've been ~~slacking off a bit~~ wanting to make sure the design is more or less finalized. Now that I'm done with that, let's dive right into that! :)

### Power Nodes, part 2!
So, sadly [the great discussion](https://www.reddit.com/r/TypoTales/comments/pfqf38/power_nodes_design_discussion/) I hoped for when posting the last blog post regarding Power Nodes never occurred. That's fine! I'll just assume everyone loves the idea the way it is! :P Well, based on the sparse feedback I got, there won't be Guardhouses. Instead, every node will have a small passive defense value which can be upgraded via the outpost and walls.

Development is going well, although it took me a bit to figure out how to best tackle all the code changes needed to make them work. Especially the "more advanced" effects that aren't just some multipliers are still giving me some minor headaches, but luckily I don't need to implement those immediately. There's also a lot of UI work involved - plenty of new information that needs to be displayed in a somewhat efficient manner.

Every Power Node will be unique region in the world, with custom effects and a description. At launch, effects will include: 
- Resource Production Boosts
- Guild Activity (Campaign, Defend, Explore) Bonuses
- Factory Focus Boost
- Factory Production Yield Bonuses

The way it's implement now, these effects can be mixed & matched as I see fit. There won't be immediate tiers, but some nodes will definitely feature better effects than others. I'll add more over time, depending on how things evolve.

Obviously there is a lot of additional UI involved for all the things you can do. Let's have a run through the things implemented right now:

First of all, discovering nodes is fairly straightforward, they'll just pop up during exploration like sites do right now. You can then view your intel with `/intel`. Note that intel never expires, but it also won't refresh - so the ownership data in your intel overview might be stale. You can refresh it by either randomly discovering the node again during exploration or sending an attacker there. The latter will obviously notify the current owner of the guild. An alternative would be to have another guild share their intel with you.

Attacking & taking over nodes isn't yet implemented, but I'll use some sort of point-system there: A node's outpost level indicates it's "lives". A successful invasion will lower that by one. The owning guild now has to invest resources in order to repair it. If all of those lives run out, we'll have an ownership change following the same rules as detailed in [the last blog post](https://typotales.com/posts/20210901-august-review-2021). Neutral Power Nodes will always be claimed directly after one attack.

Once taken, you can use `/transport` to transfer items there. Note that only processed Materials (so Wooden Beams, Cut Stone, Nuts & Bolts) can be transported, and there's a hard limit on a guild's total transport capacity – owning multiple nodes will be a bit more complicated to manage, but in the future there'll be a guild building to help out with that! Owned Nodes will appear in the territory overview, including information on ongoing transports.

Finally, you can use those materials to upgrade your outpost or the node itself. If you upgrade the node, it's effects will grow stronger! Node upgrades will also remain mostly intact on ownership change, but I might lower the value by one each time ownership changes.

#### How to motivate People to fight for nodes
Having this option for guild pvp is nice and all, but how to make sure that there'll actually be some conflict?
- Scarcity: Every Power Node is unique and manually created by me, so there won't be an infinite amount.
- Positive Effects: Some of them will be fairly desirable, such as increased campaign strength or (in the future) exclusive access to special adventures.
- Leaderboards: There will be two rankings for "longest Power Node ownership", tracking both lifetime and current node durations. Only way to climb that ladder is to nudge others off of it!
- Ownership History: The game will keep track of who owned a node (and for how long), which will be directly visible in a power node's description.

<br>
Overall, this is by far the biggest update I've implemented during this playtest. Let's hope it will be good in the end! But enough about Power Nodes! You'll very soon be able to experience them yourselves. :)

### Long-term server performance & Ghost Hunting
In the past we've had pretty much daily updates (will return back to that soon!), which means very regular server restarts. A month or so in, there was a weekend where I wasn't able to push an update for a couple of days and then the servers crashed – looking at the logs, there were some weird lag spikes going on, growing larger the longer the game ran uninterrupted:
![Lagspikes]({{ '/assets/images/21/lagspikes.png' | relative_url }})<br>

Looks fun, right? Well, it was somewhere in the guild service, I just didn't know where and had to look all over the place, changing and optimizing some things that might cause leaks to some extend, although in most cases I already knew that those spots could never cause such a huge spike in a service that's just processing the guild ticks and messages to the guild bot... wait, messages to the guild bot? Yeah. As it turns out, Telegrams "privacy mode" gets disabled as soon as a bot receives admin privileges. Therefore I process all those messages on my backend - but that alone shouldn't cause those weird spikes, so I ignored it for way too long. Then, one day whilst investigating some other issue, I noticed this:
![Oops!]({{ '/assets/images/21/bucketsofdoom.png' | relative_url }})<br>

Turns out that I implemented performance Monitoring for each individual command at some point in the past – a good idea overall, buuut... every single message which got processed by the guild bot had it's own metric created. In the above graph, you can see the amount of "buckets" tracking response times for individual commands. Given that some guild chats are fairly spammy, after some days of uninterrupted operation, the Guild Service had over 5000 individual "commands" it kept track of. Those are queried by my monitoring stack in regular intervals, and processing all of them caused those insane spikes. An interesting pattern to keep in mind for the future!

It was easy to fix, unknown commands now get thrown into an "unknown command" bucket instead of being kept track of individually and, even two weeks in without an update or server restart, curves look way more flat now. :)
![Fixed it!]({{ '/assets/images/21/fixedbuckets.png' | relative_url }})<br>

### A quick look ahead
So, what's next after Power Nodes are finished? I got one word for you: *Content!* It's been way too long since new adventures where added (partially because I *really* was slacking off a bit) and I'm going to remedy that this month. Also expect more companions (I've heard you want to catch a certain phoenix chick?) and (maybe?) finally some new equipment!

<br>
<br>
*And that's it for this month. Have a spooktacular October, everyone! :)*