title: Sleep Stream Online
date: 2011-02-28 23:05:09 

After writing up the [Zeo post yesterday][1], I decided to see if any
projects involving the Zeo and the arudino or raw streaming libraries
had happened yet. Sure enough...

![](//images/2011-02-28-sleep-stream-online/sleepstreamonline.png)

[SleepStreamOnline][2] is a project by one of the interns at Zeo that
uses the [Zeo Raw Data][3] library in order to stream your sleep data
in real time to a website. That website then relays the data to other
registered users, currently through a flash interface.

While the site still looks to be in the early stages of development,
this could turn into something quite interesting for creative types,
especially if a nice streaming API is added (this shouldn't be too
difficult with the relatively low amount of information transfer per
Zeo unit). I'd personally love to be able to feed real time sleep data
of a group into [Max/MSP][4] for live performance. Not to mention, if
the user base becomes large and international enough (it's currently
at 10 users, so it's got a bit to go), no matter which timezone
you're in, you could always hope to catch a real time stream coming
from somewhere.

There's some interesting privacy issues inherent in transfering this
data, but I'm going to let someone else write about that. I'm happy to
enjoy the creative potential here. It's like [pachube][5] for dreaming!

[1]: http://www.openyou.org/2011/02/27/zeo-and-open-source-software-arduino-development/
[2]: http://www.sleepstreamonline.com
[3]: http://developers.myzeo.com/data-decoder-library/
[4]: http://www.cycling74.com
[5]: http://www.pachube.com
