---
layout: post
title:  "The need for speed"
categories: coding gamedev
tags: computer gaming trekwar gamedev software java waybackmachine
---
I finally got around to implement the new ship system for the [Trekwar](http://www.trekwar.org) game.

Ships are no longer static objects with fixed attributes (weapon, shields, armor, etc..).

All ships are no based on a specific hull, which has some base armor and crap, + X number of slots you can put equiptment in. Below is the starting ship of all factions in the game:

![Ship slots](images/2009-trekwar_slots.jpg)

*If you noticed that this is the design of a Maquis raider, give yourself a cookie!*

I got lot of Starship components to add, and so far I’ve just added ‘Warp Core’, ‘Colonization module’, ‘armor’, ‘beam emitters’ (phasers) and ‘Shield emitters’.

One new thing I implemented today was ship speeds. Unlike in Civilizzation / Birth of the Federation, where units can only move 1 or 2 tiles each turn. Ships in Trekwar can have a speed of 1.0 (which lets it always move 1 tile each turn) or 0.7 like the colonization ship in the screenshot below:

![Ship movement speed](images/2009-trekwar_race.jpg)

The upper most ship is a scoutship with a speed of 1.0

The lower ship is a colonization ship with a speed of 0.7, that means when it starts moving it will generate 0.7 movement points.. this is not enough to move a full tile. The next turn it generates 0.7 more and then gets 1.4 movement points.. It can the move 1 tile, and has 0.4 movement points “to spare”.. On the third turn in this example it gets 1.1 movement points and can move again..

Ships with a speed below 1.0 will occationally “miss” a movement while moving a distance.  Ships with speeds greater than 1.0 will occationally move 2 (or maybe even 3) tiles in a single turn.
