title: Taking over Emokit lead
date: 2011-02-25 15:01:09 

They say he who dies with the most maintainerships... dies very tired.

![](/images/2011-02-25-taking-over-emokit-lead/emotiv.gif)

The [emokit][1] project, started by [Daeken][2], aims to provide a
free driver to access raw data coming from the Emotiv EPOC
headset. However, he's been really busy being awesome elsewhere
lately, so after picking up the decode key for the special pre-release
unit, writing a C implementation of the library, and fielding some
support emails, I (Kyle) have finally just gone ahead and taken the
lead maintainer role on the project.

Many thanks go to [Daeken][2] for the initial work on getting the
library and community together, and hopefully he'll come back to visit
at some point.

The new main repo is at

[http://www.github.com/qdot/emokit][1]

Next big steps for the project are:

* Isolating the power level readings
* Finishing up and formalizing the C library
* Getting a full v0.1 release out

I also develop the [np_epoc external for Max/Pd][3]. I expect that I'll
be updating the external along with anything we get done with the
headset itself, so keep an eye on that [on my personal externals page][4].


[1]: http://www.github.com/qdot/emokit/
[2]: http://daeken.com/
[3]: http://www.github.com/qdot/np_epoc/
[4]: http://www.nonpolynomial.com/externals/
