---
title: Service Information
layout: post
date: 2016-08-17 15:00:00
description: "I am not going to sell the actual bot. Rather, I am going to be hosting a fame train bot ***service***."
---

I am not going to sell the actual bot. Rather, I am going to be hosting a fame train bot service. 

I'm sure you are familiar with proxies and making the ROTMG client connect to a proxy as opposed to the ROTMG game servers. My Fame Train Service is going to be like a proxy. But instead of making the ROTMG client connect to a local proxy that is running on your computer, you will be connecting the ROTMG client to my Fame Train Bot proxy which is being hosted on my servers. The proxy will move for you, pick up loot for you, join realms for you, disconnect from oryx castles for you, etc - it is fully automatic. All you have to do is connect to the proxy with my modified swf. Having said that, at its current stage in development, the connection can be somewhat unstable and you might get disconnected from the ROTMG server. You will have to press the "Play" button again manually. This happens on average once every few hours. I am looking in to making the service more stable and I am looking for solutions that will automatically reconnect your client if you are disconnected. Also, I will provide .ahk scripts if needed that will press the button for you, at the expense of controlling your mouse for a few seconds.

There is going to be a bridge server that will be running locally on your computer that will connect you to my servers. The bridge server is for things like authenticating to my server (my server will not let you use the service unless you are authenticated and have got a valid subscription). In other words, to access my server, all you need to do is: run the bridge program on your computer, login in to my server with an account that you will have made when acquiring the subscription (not your ROTMG account) and then, with the modified .swf client, connect to the bridge (and thus to my fame train service).

In the future, I may also provide an automatic fame training service in which the .swf is run on my servers as well. For now, however, you will have to run the .swf on your computer yourself - you might also want to keep your computer running. Don't worry, though, the .swf file will be able to run in the background and minimised. If you are using the .ahk script that I mentioned, however, the script will bring the window into focus from time to time to check if you have been disconnected and to press the "Play" button.

If you would like, I will also be willing to provide my modified .swf that also does not display your name in the GUI anywhere (apart from if you speak in the public chat). Also, if you want, you can check the code of the modified .swf. It will not contain anything malicious. After all, <a href="{{ site.url }}/2016/08/security/">I take security very seriously</a>