title: libfitbit announcement and progress
date: 2011-02-21 22:48:09 

I've spent the past couple of weeks working on [libfitbit][1],
library that provides hardware access to the [fitbit health device][2]. The
current goal of this library is to provide a mechanism to build an
open source data aggregation client, meaning linux-using fitbit owners
can finally sync their hardware with the website.

![](http://images.nonpolynomial.com/openyou.org/blog/2011-02-21-libfitbit/fitbit.jpg)

For those that aren't familiar, the fitbit is a clip-on accelerometer
that features a nice little OLED screen and wireless data
synchronization capabilities via ANT hardware. 

Currently, [libfitbit][1] is written in python, and implements most of
the fetching and uploading protocol of the fitbit, enough that web
synchronization via linux has happened successfully (minus a couple of
commands from the server that I can't seem to send to the device
correctly). Once all commands are sending correctly, the next goal is
a C version of the library, as well as some demo applications of
"real-time" access, such as a smart "get up a move" detector (that
warns you when you've been sitting for more than a certain period of
time, but also takes into account when you've moved by reading the
fitbit). I will also probably split out the ANT python protocol
library into its own repository, since it'll be handy in other projects.

[fitbit][2] themselves have [released their own API][3], but this is only
for accessing their web services, and does not cover actual hardware
access. However, the web API and libfitbit could easily be used
together to create new and interesting interfaces combining the
hardware and fitbit's data services.

One of the other main goals behind this is to create a centralized ANT
sync dongle so that multiple devices can sync to a single USB
dongle. I'm honestly not sure if this is possible (my knowledge of the
RF side of ANT is still cursory at best), but I don't see why not, and
it's far better than having to keep track of a ton of different
dongles across multiple machines.

[1]: http://www.github.com/qdot/libfitbit
[2]: http://www.fitbit.com
[3]: http://dev.fitbit.com/
