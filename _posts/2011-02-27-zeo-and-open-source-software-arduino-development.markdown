--- 
title: Zeo Sleep Tracker and Open Source Software/Arduino Dev
date: 2011-02-27 22:05:09 -08:00
layout: post
---

**UPDATE 2013-06-11:** Zeo has shut down, and all sourceforge/myzeo
  links no longer work. All of the APIs are now available on the
  [OpenYou Github account](http://github.com/openyou). For more info,
  see
  [the Zeo API OpenYou post](http://www.openyou.org/2013/06/11/zeo-firmware-and-raw-data-api-on-github/)

I recently obtained a [Zeo Sleep Tracker][1], and was ramping up on
reverse engineering it. It's always nice to find out during your first
search for that task, that the company themselves released libraries
and you don't have to do the work.

<CENTER><A HREF='http://www.myzeo.com'><IMG SRC='http://images.nonpolynomial.com/openyou.org/blog/zeo-headband.jpg' /></A></CENTER>

The Zeo is basically a [low sensor count EEG][8], similar to the
[Neurosky][2] headset, except with a much better form factor to sleep
with than headphones.

Zeo themselves put out two libraries you can use to access data from
the device. There's the data card decoder library, that allows you to
access data from the SD card that sleep data is logged to. This is
available in a Java library at

[http://developers.myzeo.com/data-decoder-library/][3]

There's also an auxiliary serial port on the back, that can be used
for real time data acquisition. There's a python library available to
do that at

[http://sourceforge.net/projects/zeorawdata/][4]

The Zeo picks up a more band-focused signal than Neurosky or Emotiv,
since they're just looking for resting versus a full spectrum, but it
could be quite interesting nonetheless, especially to relay something
like the arduino... [Which someone has apparently already done!][5]

<CENTER><a href="http://www.flickr.com/photos/30874308@N06/5468958406/"
title="Zeo with Arduino by eok.gnah, on Flickr"><img
src="http://farm6.static.flickr.com/5100/5468958406_aa0659a7c3_m.jpg"
width="240" height="179" alt="Zeo with Arduino" /></a></CENTER>

This setup allows you to hook the Zeo directly to an
[arduino development board][6], which could then be used for setting
sleep music, LED firing for lucid dreaming masks, and other sleep
based projects.

There's more development information on [Zeo's message boards][7].

[1]: http://www.myzeo.com
[2]: http://www.neurosky.com
[3]: http://developers.myzeo.com/data-decoder-library/
[4]: http://sourceforge.net/projects/zeorawdata/
[5]: http://blog.myzeo.com/forum/zeo-raw-data-library/zeo-and-arduino/
[6]: http://www.arduino.cc
[7]: http://blog.myzeo.com/forum/
[8]: http://blog.myzeo.com/5-steps-to-phasing-sleep/
