--- 
title: Emokit, libfitbit project updates
date: 2011-03-13 17:27:09 -08:00
layout: post
---

After both spraining my ankle and getting a cold, I decided it was
time to spend a weekend on programming self quantification hardware
libraries instead of producing data for them. Some people would
probably call this "downtime," but that's not a term I deal with well.

In the [emokit][1] realm:

* Windows support in the C driver is done and confirmed working,
  though for some reason the device enumerates as 2 devices, since
  there's 2 HID interfaces.
* Found out there's another VID/PID pair for the usb dongle, which
  makes life slightly more difficult. The issue is outlined in
  [this github issue on Daeken's github repo][2]. I'm now working with
  someone who has this dongle to try to get both working at the same
  time.

The hope is to get two of the major portions of [emokit][1] knocked
out ASAP:

* Auto-headset type detection
* Searching for all possible VID/PID pairs

After this, the library should be usable in a v0.1 state while we
figure out things like power levels.

Next up, I did a little bit of work on [libfitbit][3]. It's now
transfering data more reliably due to fixing how tracker resets are
handled (they may or may not send 2 packets sometimes). I still
haven't gotten sending of data to the tracker working yet, but once
that's done, hopefully there'll be a v0.1 release of the python
version, as I outlined in the last post.

[1]: http://www.github.com/qdot/emokit
[2]: https://github.com/daeken/Emokit/issues#issue/6
[3]: http://www.github.com/qdot/libfitbit
