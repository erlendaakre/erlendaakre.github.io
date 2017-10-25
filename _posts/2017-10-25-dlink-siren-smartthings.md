---
layout: post
title:  "D-Link DCH-Z510 Siren with Smartthings"
categories: home-automation
tags: smartthings security alarm home home-automation smarthome 
excerpt: Getting a D-Link Z-wave siren working with smartthings
---
I just got my D-Link DCH-Z510 Siren and trying to set up a rudimentary alarm system by connecting it straight to smartthings (not using any D-Link apps or products.

### First step
Impatiently connect plug in the siren, discover new devices. Smartthings discovers it as "Aeon Labs Siren (Gen 5)".

In the app I can turn it on and off, it makes a lot of sound (well, 110 decibel). 
However going into it's settings I'm unable to change the siren sound, no matter which one it's set to (1-5) it sounds the same.

### Second step
To be fair I was not expecting step 1 to work particularly well, time to try using the [custom device handler](https://github.com/fuzzysb/SmartThings/blob/master/devicetypes/fuzzysb/dlink-dch-z510.src/dlink-dch-z510.groovy)
Grab that code and fire up the [SmartThings IDE](https://graph.api.smartthings.com).
