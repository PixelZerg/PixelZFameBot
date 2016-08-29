---
title: No Beta Testing 
layout: post
date: 2016-08-29 11:14:08
description: "A turn of events means that closed beta testing is no longer required and the release of PixelZFameBot has gotten closer!"
---

The reason why I thought I needed to do closed beta testing is because my program, PixelZFameBot was super buggy - it was crashing all the time and there seemed to be a lot of bugs. I was absolutely ripping my hair out trying to patch all these bugs and so I decided I needed some help getting all the exception reports. However, yesterday, I made a striking discovery - there was a bug at the ***BINARY LEVEL*** in my program! I found the error and I fixed it and the improvement of stability is like night and day. The amount of time before a crash went from a couple of seconds (or a couple of minutes if you are lucky) to no crash at all within the 2 hours that I tested the improved version yesterday.

The bug occurred because I was AES encrypting every single packet between the bridge and the PixelZFameBot Server. The encryption messed up the timing and sometimes even skipped bytes. To solve the bug, I changed the model of bridging the packets from the ROTMG server to the PixelZFameBot server. This new model works perfectly, however, it does not involve any buffers. If you know anything about programming, you would know that this means that there is no way for me to AES encrypt the packets now. In other words, the packets will no longer be AES encrypted. Only the important packets like when you are authenticating with the PixelZFameBot authentication server will be AES encrypted. But lets be honest, encrypting every single packet was major overkill and frankly, slightly stupid because it was bound to cause unnecessary overhead.

Thank you so much to all the people that signed up to be a beta tester, it truly is heart warming to know that so many would be willing to help improve the state of the bot. Sorry for getting everyone's hopes up. However, closed beta testing is no longer necessary. On the bright side, nobody gets to try out PixelZFameBot before everyone else and has an unfair advantage. Also, I can start focusing on some features of the bot that I'm sure you people will certainly want, though is lacking in PixelZFameBot at the moment - such as:

- customising item picking up values - you might want the item picking up module to favor a certain item.
- character-specific - stuff like autonexus %, the point above, etc. Each character connected to PixelZFameBot can have different settings.
- a chat filter
- a "status" and "current module" so you can see what PixelZFameBot is "thinking"
- email you a password reset code if you forget your password
- make the "PixelZFameBot Launcher"
- etc...

and also, I have still yet to import the WINAPI invokes, AutoIt commands and the AHK scripts to reconnect the client in the case that it does lag out. I also need to make a website for PixelZFameBot.

But most importantly, this means that I will no longer need to go through closed beta, instead there will be an open beta of sorts - this that means the amount of time before the public release of PixelZFameBot has been decreased greatly. Start getting excited, people! (though, as you saw, I still have a lot of work to do.)