--- 
title: OpenYou Github Organization
date: 2012-10-21 15:57:20 -08:00
layout: post
---

I've finally gone ahead and moved most of my health driver repos, as
well as the repo holding the openyou.org blog, to the
[OpenYou Organization on github][1]. Over an indeterminate amount of
time in the future, I'll be flipping the READMEs, and possibly the
licensing, to reflect OpenYou also.

The hope here is to get more community involvement in drivers for
health equipment. Up until now, the repositories have lived on
[my personal github account][2], which, while great for my coderwall
badges, means that I'm primarily responsible for support. Ask anyone
who's emailed me actually _asking_ for support, and you'll find out
how well that's gone so far.

While I do get and try to service pull requests on my drivers,
sometimes it takes me weeks or months, or else I do things out of
order and end up conflicting people's patches. My hope with moving
these to an organization setup is to allow developers that are
interested to help out with maintenance of these projects.

I'm already starting to see this in action, as there's now a developer
on the [emokit][3] project working on porting the C library to HIDAPI.
I'd like to get battery power and signals in soon too. There's a bunch
of stuff to be done on things like [libfitbit][4] and [libomron][5]
too.

Moving this stuff forward shouldn't depend on the amount of free time
I have. If you're interested in becoming a developer with commit
rights on one of these projects, file an issue in the project you're
interested in working on.

[1]: http://www.github.com/openyou 
[2]: http://www.github.com/qdot
[3]: http://www.github.com/openyou/emokit
[4]: http://www.github.com/openyou/libfitbit
[5]: http://www.github.com/openyou/libomron
