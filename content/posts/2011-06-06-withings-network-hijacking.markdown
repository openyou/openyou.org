title: Withing Scale Network Hijacking
date: 2011-06-06 22:01:19 -08:00

The [Withings Scale][1] is a pretty simple piece of hardware. Set it up
on your wifi network, weigh yourself, and it instantly sends your
weight to the Withings website.

![](http://images.nonpolynomial.com/openyou.org/blog/withings.jpg)

Now, as Withings isn't really taking and analyzing a ton of data, it's
(apparently) fairly trivial to pull all the needed data from their
website. However, there are those who aren't completely happy with
that solution, and who also don't want to deal with the slow flash
interface.

The people at
[Proxilium decided to reverse engineer the network protocol][2], doing
a full trace on the communications between the scale and the home
website, and extracted all of the data the scale sends to the
website. Not only that, he shows how to set up alternate DNS rules to
route off calls to the website to a local webserver, so you can have
your own data store. Neat!

[1]: http://www.withings.com
[2]: http://www.prolixium.com/mynews?id=915
