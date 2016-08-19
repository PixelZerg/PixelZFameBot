---
title: Updated Proxy System
layout: post
date: 2016-08-19 19:02:17
description: "Introducing my new, elaborate proxy system. This time, if someone were to get ip-banned whilst using PixelZFameBot, it will be only *that person's* ip being banned and not every single person using the service"
---

NB: You might want to read this article first before proceeding if you have not already: <a href="{{ site.url }}/2016/08/serviceinformation/">Service Information</a>

Here is a diagram representing what I had in mind originally for the PixelZFameBot service:
<div class="jimg"><img src="{{ site.url }}/public/poststuff/proxysystem/fameservicelinear.png"></div>

However, there is a *fatal flaw* with this setup. If, hypothetically of course, someone were to get ip-banned whilst using PixelZFameBot, the PixelZFameBot server's ip would be the one that is banned. This is because in the eyes of the ROTMG servers, the PixelZFameBot server is the one that is connecting to the ROTMG servers and so the ip address to that should be banned.

To avoid this issue, the PixelZFameBot service will now use a far more elaborate setup which looks like this:
<div class="jimg"><img src="{{ site.url }}/public/poststuff/proxysystem/fameservice2.png"></div>

To briefly explain the diagram, the red lines represent the outgoing packets and the blue lines represent the incoming packets. As you can see, everything is the same as in the previous setup, however, in this setup, the PixelZFameBot server will send the modified packets back to the **Local Bridge** and then the local bridge will connect to the ROTMG servers. Now, in the eyes of the ROTMG servers, the one that is connecting to the ROTMG servers is the **Local Bridge** (which is running on your computer so i.e YOU). That means the ROTMG servers will send the outgoing packets to the Local Bridge, which will then get sent to the PixelZFameBot server where it may or may not be altered. Then the PixelZFameBot will send that back to the LocalBridge, which will pass that onto the ROTMG Client. So now what this means is that since in the eyes of the ROTMG servers, the Local Bridge is the one connecting to the ROTMG servers, if you ever get ip-banned whilst using the PixelZFameBot service, it will be only your ip-address that is ip banned.

Obviously, there is some risk that when using the bot that you will be banned. I will not be held viable if you do get banned. It is up to you to make sure that you are not doing something overly stupid in order to get yourself banned like running 20 accounts all using the PixelZFameBot service. Personally, the account that was used in the live-stream at the time of writing has only ever been using PixelZFameBot when it is online and it has been 22 days since its creation (in which it has accumulated 60 stars) and has still not been banned.

Going back to the PixelZFameBot setup, I have just now finished my first working prototype of this connection system and it seems to be working well:

{% include youtubevid.html code="qHttX71tU9E" %}

Good progress has been made on the development of this service! :smile: