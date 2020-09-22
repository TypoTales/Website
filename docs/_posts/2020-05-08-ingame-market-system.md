---
layout: post
title: The Ingame Market
description: 
summary: 
---

Over the past week I've been busy implementing the in-game market system. I'm pretty satisfied with how it turned out, so I hope people will enjoy and use it once the game is out - the economy will be purely player driven, with adventures and gathering activities only rewarding players with materials to craft and upgrade their stuff. Hope it works out that way. :D

Dunno how interesting this is going to be, given that it's a fairly... normal market system you can find in most other MMOs, but let's take a deeper look at it nonetheless:

First of all, the `/t` command shows all available information to a given item, like this:

![Market Overview]({{ '/assets/images/marketSlashT.jpg' | relative_url }})

The game will display the 5 best available buy & sell orders first, though if you want to see more orders, you can use the buttons below the message to view more. Furthermore, if the item is an armor or weapon, you'll be able to filter results by upgrade level with the "+X" buttons. Finally, there are some statistics - sale volume, average price, and (soon) also lowest & highest price over a certain time frame (right now it's 24h, though I might make that adjustable in the future). Those stats won't be completely real-time since I'll probably have to cache the result for some time to avoid lag spikes if many people browse the market at once.

Let's say you find a good deal or want to create a new order - for that you can use `/wtb` or `/wts`. The game will automatically match your price with what's available on the market and buy/sell the best offer - if no offers match your request, you'll create a buy/sell order instead. 

Last, but not least, you can use `/orders` to view and manage your own orders. Sadly, I'm not yet done with that, so there's no screenshot for that - though you'll be able to filter your orders by item type (consumabes, weapons, etc.) and delete them. I might also throw in an option to get notified (or disable notifications) when an order is filled for all or individual orders.

Right now, there are no plans on limitations regarding a maximum amount for orders or inventory space - though if I decide to add one, it will start small and be upgradable by a combination of common materials and ingame money. Might be a nice resource sink for traders.

Oh, and one more thing - you don't have to remember all the item ids! It was fairly simple to plug in the item finder that I've originally created for the `/d` command (which displays information about literally anything in the game), so you can search for items by name as well - if there are multiple matches, you'll be shown a neat selection like this:

![ItemFinder]({{ '/assets/images/marketSlashTitemFinder.jpg' | relative_url }})

That's it for today. Hope you are looking forward to get rich through the market once the game launches! :) In two weeks I'll either take a look at the encounter system or present you the very first equipment sets.