title: libfitbit Hangups
date: 2011-08-07 19:34:29 

First off, hello to everyone who found us through the MIT Tech Review
article or Ubuntu Community talk! Been a bit slow around here lately,
but hoping to get things booted back up.

It seems the most requested thing at the moment is a finalized version
of [libfitbit][1]. Currently, we're at v0.0.1, which was released in
February and hardly worked. There's been a lot of progress since then,
and we are now able to replicate full communications with the
tracker. There's really just one problem left with the library, and
that's the subject of today's post. 

So, unless you're into specifics of the implementation of the ANT
protocol, you can probably skip the rest of the post. However, if
you're interested in helping me kill the last bug before I can start
making distributable, read on.

I recommend having the [ANT Protocol Specification][2] open while
following along, as I'll be talking about packet types quite a
bit. Also, if you have any comments, please leave them on the
[github issue about this problem][4].

**UPDATE:** And, 2 hours after I post this, [I fix it myself][4]. I
wasn't resetting the USB device correctly, which meant we were getting
weird configuration conflicts from the last session run. Fixing the
device reset clears this, and libfitbit will now retreive information
multiple times without having to completely un/replug the key. I'll
write up a "rest of the things I need to do" post tomorrow to let
everyone know what's next.

<!--more-->

Whenever libfitbit connects to the tracker, the first transfer after
plugging in the USB goes fine. We start communications with an ANT
reset message, and we always get back a 0x6F package (Startup Message)
with a payload of 0x00 (POWER_ON_RESET), which is what we expect since
we just powered on the ANT stick. We then continue on through
establishing a communications channel, running a beacon signal to find
the tracker, and other steps as laid out in the [fitbit protocol document][3].

The problem comes in on the second run of a libfitbit based
utility. We try and reset the device, but instead of getting back a
0x6F packet, we usually receive something that looks like a bulk data
receive packet, like we would expect back from a bank
transfer. Further executions the utility will result in the same,
until the point where the receive command from the reset completely
times out, and continues to do so. The only way to fix things at this
point is to unplug/replug the ANT stick, at which point things work
fine again, for one round of communication.

The actual fitbit client doesn't have to deal with this due to the
fact that it grabs the device right when it starts up, and doesn't let
go until shutdown. I suppose I could try stopping and restarting the
service with the base plugged in while watching an analyzer, and that
may be my next step.

This bug is the major thing holding up library development right
now. Until this is fixed, I can't reliably run multiple sessions with
the fitbit, and having to replug the USB stick isn't a viable
solution. I'm pretty sure I'm missing something about how connections
should end or restart, but progress on this one is slow so far.

[1]: http://www.github.com/qdot/libfitbit
[2]: http://www.thisisant.com/images/Resources/PDF/1204662412_ant%20message%20protocol%20and%20usage.pdf
[3]: https://github.com/qdot/libfitbit/blob/master/doc/fitbit_protocol.asciidoc
[4]: https://github.com/qdot/libfitbit/issues/8
