title: Project Updates - Liblightstone and libomron
date: 2011-03-27 21:25:09 

Time for what I do best, more project updates!

First off, after 3 years of brokenness, liblightstone may see full
stability for multiple devices in upcoming v1.5.

![](//images/2011-03-27-liblightstone-libomron-project-updates/wildivine2-m.jpg)

The lightstone is a USB device that comes with the
["Journey to Wild Divine"][1] video game. The point of the game is to
teach users to relax and breath deeply. However, with the game itself
working sporatically thanks to being based on a very old version of
Director, actually finding peace with WD rarely happens.

[liblightstone][2] was established in 2006 to help owners of the
lightstone access data from the device in an open source, cross
platform way. However, it has been plagued with bugs when trying to
use multiple devices on the same machine, and the release of an
updated lightstone with different USB VID/PID pairs caused
problems. After finally obtaining one of the newer lightstones last
week, I've fixed the aforementioned problems and hope to release v1.5
soon. I hope these will make the driver stable enough to call the
hardware access project done for the foreseeable future.

v1.5 will hopefully be released in the next couple of days, after I do
some testing across windows machines. I've been getting odd
differences in device enumeration between machines with the WDK
installed versus without.

The USB access code from liblightstone is also used in projects like
[libomron][3] and [emokit][4], so these bugfixes will be finding their
way to other projects soon.

[libomron][3] is also going to be seeing some work soon as we try to
continue it toward v1.0.

<CENTER><A HREF='http://github.com/openyou/libomron'><IMG SRC='//images/2011-03-27-liblightstone-libomron-project-updates/omron-pedometer.jpg' /></A></CENTER>

[libomron][3] is a driver for Omron based USB devices, such as the

- HJ-720ITC Pedometer
- HEM-790-IT Blood Pressure Monitor

It currently only covers those two pieces of hardware, as well as
their foreign counterparts (like the M10-IT blood pressure
monitor). However, it looks like most of Omron's equipment uses the
same protocol, so the base of the library is extensible to new
equipment as it comes out.

While the omron equipment isn't as flashy as, say, the [fitbit][5],
it's far cheaper ($20 for omron's USB pedometer if you find it on
sale, versus $99 for a fitbit). 

[libomron][3] is currently approaching v1.0, with a few things left to
be done in order to get multiple devices working (same issue as
liblightstone had), as well as getting device clearing
working. Finally, we're hoping to have a simple XML/JSON/CSV data
exporter available so it can be easily run by other programs with no
need for interfacing at the source level, unless you want neat
progress bars or something. Everyone loves neat progress bars.

[1]: http://www.wilddivine.com
[2]: http://github.com/openyou/liblightstone
[3]: http://github.com/openyou/libomron
[4]: http://www.github.com/qdot/emokit
[5]: http://www.fitbit.com
