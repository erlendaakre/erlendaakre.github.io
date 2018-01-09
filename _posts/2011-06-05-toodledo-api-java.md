---
layout: post
title: "Toodledo API (simple java version)"
categories: coding
tags: coding software java toodledo list bugs xml api dom waybackmachine
---

I wanted to get a list of all the bugs for my Star Trek game, that I have registered at Toodledo and have them listed on the Trekwar wiki.

Toodledo offers a nicely done API, but there was no java implementation, there were a couple of unofficial ones, but I decided to write my own very simple basic program for connecting to Toodledo and getting all the tasks as XML, and parsing them into a simple Java object. So if you’re doing something similar, this program might be a nice place to start. To keep it as short as possible, comments and exception handling is pretty much not there :)

<script src="https://gist.github.com/erlendaakre/f0b23435431a2b41346a567c97f82a54.js"></script>

**Note:** This program was made to run once per hour. Running it many times in a row will cause Toodledo to ban you for about 1 hour. When that happens there will be a IndexOutOfBoundsException -7 from the method that gets the session token. This can be fixed by saving the token you get between requests, and not asking for a new one each time (which is what causes the short ban).

