---
layout: page
title: About
---

PixelZFameBot is a  fame train bot for ROTMG made by me, PixelZerg. It started out as a proof-of-concept program, but it had a sudden surge of popularity because of forum websites and this live-stream video that I uploaded on my channel: 

{% include youtubevid.html code="ppj3XtiOBmU" %}

Because of that, I am now working hard on polishing up the program and improving the code so that I can release it in the nearby future. Please understand that creating a fully polished service out of a proof-of-concept program that I made without putting much thought into essential things such as code handling, the user interface, efficiency, etc is not something that can be done overnight. Thanks for everyone's patience.

## How it works:
1. Move to fountain if hp is not full
2. Spam UseItem on realm portal (which can be found in the update packets)
3. Once joined realm, remember the realm IP so next time you don't need to wait for it to open and join it directly
4. Look at all the players on the map, divide them into clusters using basic cluster algorithms which basically group people on how far apart they are from one another
5. Find the densest cluster (the cluster with the most people) - but if the cluster is more than 600m from the centre of the map, ignore it (ignoring beaches)
6. Calculate the centroid of the cluster (the player in the closest to the mean vector of all the vectors (players) in the cluster)
7. Teleport to the centroid every so often
8. Follow that player around.

It also replies to PM's using a ChatBot AI. Feel free to come online and have a chat with it (be wary that if there are too many people talking to it at once, it will ignore you because that clutters the screen).

## Which swf client is it using?
It is using the normal 27.7.X client, but I modified stuff such as people's names being blue and also the starring out of the username. If you look closely when it changes realms, you can see it says the client version is #27.7.PixelZerg lol

## How Do I talk to it?
If the bot has not received a PM in the last 15 seconds (75 ticks), it will pm the next person that speaks in the public chat "wanna be friends" and the conversation will start from there. Alternatively, you can PM it at any time if you know the account's name. Be wary that if it is talking to more than 5 people at the same time and you try to talk to it, it will ignore you for a while.

## When was the account in the livestream made?
The account was made specifically for this livestream so it is only a couple of days old.

## How does the autoloot work?
The autoloot feature works by walking towards the bag and picking it up. At the start, it picks up everything and everything and then once it's inventory is full, it will swap out stuff and replace it with the thing in the bag if the thing in the bag is of greater value than what it is swapping it with.

## How is item value calculated?
The bot looks at the fame percentage of the item (it is a fame farming bot after all). It also considers pots. That is, dex,wis,vit less than spd less than att,def less than mana less than life

## Does it suicide itself once it reaches 5 stars?
No the fame train bot only fame trains and picks up bags and a few other little stuff. Everything else is manual. I am open to suggestions, though, and I may very well implement this in the future.
