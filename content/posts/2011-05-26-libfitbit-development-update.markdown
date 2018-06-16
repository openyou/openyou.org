title: libfitbit Development Update
date: 2011-05-26 22:20:12 

There's been a lot of interest in [libfitbit][1] lately, so here's a
quick update on where I am with development.

* Web client is now completely working. Was stuck on ANT burst sends
  not working, which are used to update the device time and stats like
  height and weight. Putting in a sleep between burst sends seems to
  have fixed it. Because, much like [putting a bird on it][2], putting
  a sleep in it fixes everything.
* Tested the fitbit with the [Garmin ANT Stick][3], works fine. Hoping
  to test with [Suunto stick][4] within the next week, the goal being
  to have multiple ant antennas on multiple machines, all which can
  communicate with any ANT hardware.
* Can get per-minute Step Count and Active Point Score from the fitbit

This is close to getting us to a v0.1 release, which I'm hoping will
happen next week after the [Quantified Self Conference][5]. I'm also
working on documentation and making a couple of useful utilities, such
as a linux daemon for web service uploads (yes, I realize I'm doing
fitbit's work for them, and no, I'm not real thrilled about it
either), and dumping data to json/xml.

In terms of what I'd like to see for versions after that:

* Finish the data format protocol. There's still a couple of packets
  I'm not sure about, and I haven't figured out how events (sleep,
  etc...) work yet.
* Dividing out the ANT protocol class and ANT antenna classes into
  their own library, so they can be shared between multiple device
  libraries. I'm moving toward this with the current design, but don't
  want it holding up the v0.1 release
* May a C version? I'm not exactly motivated about this since python
  works fine for me right now, but if the need arises, it could be
  nice to have around. The ANT people have actually
  [said they have little linux experience on staff][6], so I wouldn't
  be expecting their support on the library side soon
  anyways. Definitely an ownable area for anyone looking to start up
  an open source project, and there's a ton of code already out
  there...
* Whatever else people are looking for. Let me know in the
  [github issues][7] if you have requests.

[1]: http://www.github.com/qdot/libfitbit
[2]: https://www.youtube.com/watch?v=0XM3vWJmpfo
[3]: http://www.amazon.com/gp/product/B000UO9KSY/ref=as_li_qf_sp_asin_tl?ie=UTF8&tag=openyouorg-20&linkCode=as2&camp=217145&creative=399353&creativeASIN=B000UO9KSY
[4]: http://www.amazon.com/gp/product/B004YJSD20/ref=as_li_tf_tl?ie=UTF8&tag=openyouorg-20&linkCode=as2&camp=217145&creative=399349&creativeASIN=B004YJSD20
[5]: http://www.quantifiedself.com/conference/
[6]: http://www.thisisant.com/component/option,com_fireboard/Itemid,146/func,view/catid,25/id,1464/#1468
[7]: https://github.com/qdot/libfitbit/issues
