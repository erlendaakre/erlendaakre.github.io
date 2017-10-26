---
layout: post
title:  "D-Link DCH-Z510 Siren with Smartthings"
categories: home-automation
tags: smartthings security alarm home home-automation smarthome 
---
I just got my D-Link DCH-Z510 Siren and trying to set up a rudimentary alarm system by connecting it straight to smartthings (not using any D-Link apps or products.

**NOTE:** If you are trying to get this siren working and have not connected it yet, you might want to skip the first step

### First step
Impatiently connect plug in the siren, discover new devices. Smartthings discovers it as "Aeon Labs Siren (Gen 5)".

In the app I can turn it on and off, it makes a lot of sound (well, 110 decibel). 
However going into it's settings I'm unable to change the siren sound, no matter which one it's set to (1-5) it sounds the same.

### Second step
To be fair I was not expecting step 1 to work particularly well, time to try using the [custom device handler](https://github.com/fuzzysb/SmartThings/blob/master/devicetypes/fuzzysb/dlink-dch-z510.src/dlink-dch-z510.groovy)
Grab that code and fire up the [SmartThings IDE](https://graph.api.smartthings.com) and add it as a device type (I highly recommend going for the github integration)

Now since we have already connected it, let's exclude it, then add it again with the correct device handler.
Go to the device on the app, under Things, select it, click settings (cog icon) and remove. To complete the exclude double tap the small button at the back of the siren (use a toothpick or similar).
**NOTE:** The siren has an anti-tamper function, removing the back cover will be loud and surprising :D

### Third step
*To be continued...*

