title: OpenYou Projects Update
date: 2012-05-28 21:32:22 -08:00

It's really amazing how quick a year can disappear by.

Due to personal circumstances that involved
[finding a new job](http://www.mozilla.org/en-US/b2g/),
[hacking some robots](http://nonpolynomial.com/2011/11/16/keepon-control-via-kinect/),
[being in Make Magazine](http://boingboing.net/2012/03/08/make-talk-008-kyle-machulis.html),
etc... It's been a quiet year at OpenYou so far.

So, an update!

## libfitbit

[http://www.github.com/qdot/libfitbit](http://www.github.com/qdot/libfitbit)

I'm still seeing pull requests to libfitbit! The library has become
somewhat more stable, though we're still plagued by issues with the
base station locking and not communicating until it's
unplugged/replugged. I'm not sure if this is an issue with the fitbit
base station or with my python ANT library. It's something I hope to
look into soon.

I'd also like to get a Fitbit Ultra at some point, to get altimeter
readings into the system.

## emokit

[http://www.github.com/qdot/emokit](http://www.github.com/qdot/emokit)

As of today, Emokit for the Emotiv EEG sees a major update, at least
in terms of protocol documentation. We now have access to the sensor
quality levels and battery power levels, the two portions we'd been
waiting on in order to finish the library and release v1.0. I've
created
[a protocol document that's available in the github repo](https://github.com/qdot/emokit/blob/master/doc/emotiv_protocol.asciidoc),
and would like to get this pressed into code ASAP.

In less new-featurey but important maintenancey issues, I'm also
planning on moving the library to HIDAPI, which should solve a lot of
the crossplatform issues reported in the repo. I'd also like to finish
the OpenVibe bindings, which I got started but then fell off on due to
above mentioned circumstances.

## libfuelband

[http://www.github.com/qdot/libfuelband](http://www.github.com/qdot/libfuelband)

I've been permaloaned (Sorry Barry I swear I'll get it back to you) a
Nike Fuelband to work on. I did some initial proof-of-concept code a
while ago, which found some dates and what I believe are steps
recorded down to the second (the highest granularity I've seen in a
consumer pedometer thus far).

The unfortuate news is that there seems to be no good way
to access the LED array, which was my original goal. However, the
factory wipe mechanism looks like it may be a firmware reload, which
would be super handy for possibly building my own LED access
functions.

So, that's it for now. I'll hopefully be posting more about some of
the patent battles in health technology this year soon, as things have
really been heating up.
