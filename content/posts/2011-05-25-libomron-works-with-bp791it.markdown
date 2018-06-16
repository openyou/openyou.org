title: libomron Verified Working with BP791IT
date: 2011-05-25 16:31:12 

I've received from email from an OpenYou reader who purchased the
[BP791IT][1], which is the updated version of the HEM790IT Blood
Pressure Monitor from Omron.

[![](//images/2011-05-25-libomron-works-with-bp791it/bp791it.jpg)](http://www.amazon.com/gp/product/B004H44GB4/ref=as_li_qf_sp_asin_tl?ie=UTF8&tag=openyouorg-20&linkCode=as2&camp=217145&creative=399349&creativeASIN=B004H44GB4)

They've verified that this blood pressure monitor does work
with [OpenYou's libomron library][2]. So, go forth and purchase, knowing
you can still pull your data off of the device on any platform
[libomron][2] supports (which is anything [libusb][3] supports).

Please note that I've been getting a few issue reports with getting
libomron working on OS X, having to do with the kexts not causing the
device to detach from the HID Manager correctly on 10.6.7+. These
reports have been rather intermittent, but if you experience any
issues, please get in touch with me via email or [file a bug report on the github site][4].

[1]: http://www.amazon.com/gp/product/B004H44GB4/ref=as_li_qf_sp_asin_tl?ie=UTF8&tag=openyouorg-20&linkCode=as2&camp=217145&creative=399349&creativeASIN=B004H44GB4
[2]: https://github.com/qdot/libomron/
[3]: http://www.libusb.org
[4]: https://github.com/qdot/libomron/issues
