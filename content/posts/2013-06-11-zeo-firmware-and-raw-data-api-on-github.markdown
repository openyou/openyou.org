title: Zeo Firmware and Raw Data API on OpenYou github
date: 2013-06-11 13:42:20 -08:00

It appears Zeo, which declared it was shutting down in March, has
taken a scorched earth policy in terms of developer firmware and
libraries. All zeo websites are gone, and the sourceforge has been
cleared out. I still had versions of the firmware and raw data API
kicking around on my harddrive, and managed to fork the android
project before the github account disappeared. I've thrown all of this
on the openyou github account.

Zeo Firmware:
[http://github.com/openyou/zeo-firmware](http://github.com/openyou/zeo-firmware)

Zeo Raw Data API:
[http://github.com/openyou/zeo-raw-data-api](http://github.com/openyou/zeo-raw-data-api)

Zeo Android API: 
[http://github.com/openyou/zeo-android-api](http://github.com/openyou/zeo-android-api)

Since most developers are used to looking for these kind of libraries
on github, that seemed the best place to store them right now even
though I certainly have no plans of doing any upgrades to them. The
master branches will most likely stay as copies of the final versions
so that others can have a reliable base to fork from.

For developers that want web accessible documentation,
[SleepStreamOnline](http://www.sleepstreamonline.com/) (a project done
by a Zeo intern a few years ago) is still around, and has
[web documentation for the raw data API available](http://www.sleepstreamonline.com/rdl).
Assuming this ever goes down, developers should also be able to
generate their own version from the Raw Data API code using
[sphinx](http://sphinx.pocoo.org/).
