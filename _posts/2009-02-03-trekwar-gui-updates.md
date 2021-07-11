---
layout: post
title:  "Trekwar GUI updates"
categories: coding gamedev
tags: computer gaming trekwar gamedev software java waybackmachine startrek
---
Recently much of my spare time programming has gone to giving the [Trekwar client](https://github.com/erlendaakre/trekwar) a graphical overhaul.

Now I’ve managed to get most of what I broke, working again (Research and Starsystem Control), and I’ve added a glasspane that shows up and prevents the clicking of buttons (and thus creating a weird state of the client) while each tick is being processed by the server.

![fetching data from server](/images/2009-trekwar_feb.jpg)

*Currently the test galaxy is 100×100 tiles and takes about 0.5 seconds to load to cli*


![trekwar system and research view](/images/2009-trekwar_feb2.jpg)

Unlike the previous version of the game, it is now possible to have many windows active on top of the actual game map.
The system box (far left of the screen) has been changed to display more information, and next up is a complete redesign of the fleet box.

But before making the new fleet box and fleet management system, I’ll have to do some major rewrite of the internal ship system and logic, to support user created ship classes.

I’m looking forward to 8-10 hours of pure java and logic.. There is only so much Swing a man can take :)
