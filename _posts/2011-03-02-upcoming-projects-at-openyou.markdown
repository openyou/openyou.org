--- 
title: Upcoming Projects at OpenYou.org
date: 2011-03-02 23:07:09 -08:00
layout: post
---

Now that the site seems to be up and stable, I'm hoping to get back to
coding on [libfitbit][1], [emokit][2], and other things. Here's my
plans for the moment:

* Finish [libfitbit][1] python core - There's still problems with
  sending data to the fitbit as part of the final step in the website
  communications. Once this is done, I'll probably call it the v0.1
  release.
* Once the [libfitbit][1] core is done, I'm planning on dividing out
  the Python ant communication library into it's own repo since it'll
  get used by a lot of projects. This includes adding a serial access
  core along with the libusb core, so it'll hopefully 'just work' for
  some windows serial emulation devices. I may also do a C version of
  it, though I'm really not sure why ANT's own libraries aren't just
  open source at that point. The protocol is documented, would just
  save time...
* Make the fitbit real time "get up and move" application.
* Make a "fitbit finder" applicaton, so if you lose your fitbit, you
  can just hook your base station up to a laptop and carry the laptop
  around to find it. It'll give you hot/cold readings, though I'm not
  sure on the accuracy available in ping times to the tracker.
* Trying to get [emokit][2] working in [openvibe][3]. This shouldn't
  be too difficult, as [openvibe][3] already has a emotiv sdk
  communications core, and emokit exposes the same calls. Openvibe is
  just an absolutely enormous framework, so figuring out where things
  go and how to test is going to take some time.
* Do something with the [Zeo][4]. Not sure what yet.
* Currently working on getting a Garmin Forerunner. I already have a
  Suunto T3, I just need to order the USB unit for it. There's already
  drivers available for talking to quite a few of the suunto watches
  and dive equipment, which I'll be posting about soon.
* An generalized external for talking to ANT+ devices via [Max/MSP][5]
  or [PureData][6]. I do
  [a lot of work with externals for these as is][7], and got a request
  via the Max/MSP forums for this specifically. Shouldn't be too hard,
  once the ANT driver is done.

If you have any interest in helping out on these projects, please let
me know via email or comments! Help is always appreciated.

[1]: http://www.github.com/qdot/libfitbit
[2]: http://www.github.com/qdot/emokit
[3]: http://openvibe.inria.fr/
[4]: http://www.myzeo.com
[5]: http://www.cycling74.com
[6]: http://www.puredata.info
[7]: http://www.nonpolynomial.com/externals
