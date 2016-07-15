# dosbox
My Dosbox stuff

This post is from H. Peter Anvin (hpa) on http://www.vogons.org/viewtopic.php?t=22994&start=20#p209067.

A different server, possibly faster(?)
Postby hpa » 2010-12-31 @ 02:15

[OK, I already posted this as a separate thread, not familiar with this BB UI] 

Hi all, 

Not having seen this thread, I stayed up late last night and whipped out a dedicated IPX server on my own. I quickly determined that using SDL_net would not perform well, since SDL_net doesn't have support for blocking UDP receive. 

A significant criterion was that an idle server should not burn resources, so this server is designed so that when completely idle it will not consume any CPU time at all. 

It is tested on Linux; it should compile on any modern Unix system (including Mac) without modifications. It may be possible to build it under Cygwin on Windows, or it should be relatively straightforward to port it to native Windows (the biggest difference is probably the client expiration timer, which is technically optional.) 

ftp://ftp.zytor.com/pub/games/dosbox/ipxrelay-0.1.tar.gz
http://git.zytor.com/?p=games/dosbox/ipxrelay.git;a=summary

Here is another post by hpa a few weeks later.

Re: Dedicated IPXNET server.
Postby hpa » 2011-1-17 @ 06:52

I have just uploaded a new version with Windows support as well (untested, but it compiles under MinGW32). 

The .zip file contains source as well as a Windows binary. 

ftp://ftp.zytor.com/pub/games/dosbox/ip ... 0.2.tar.gz 
ftp://ftp.zytor.com/pub/games/dosbox/ipxrelay-0.2.zip
