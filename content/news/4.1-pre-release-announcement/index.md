---
title: "4.1 Pre-Release Announcement"
date: 2014-03-23T16:26:00+00:00
author: DrSlony
Tags:
- Community
- Versions
---



Dear photographers, hobbyists and package maintainers,


Soon we will be releasing RawTherapee version 4.1-stable. This is a big
deal. Everyone should read this.


Much has changed since version 3.0 of RawTherapee was released back in
July 2011. There are many new tools, the way existing tools work has
been improved, calculations are more precise, everything is faster, the
user interface had a complete make-over, everything is documented
in [RawPedia](http://rawpedia.rawtherapee.com/), and there are hundreds
of other improvements which make up the bulk of our work. As such, it
was impossible to avoid breaking backwards-compatibility of certain
things.


**Users** should be aware of changes in behavior between old and new
versions of some tools. For instance, the effects of the [Auto
Levels](http://rawpedia.rawtherapee.com/Exposure#Auto_Levels) tool have
changed (for the better), so if your old [processing
profiles](http://rawpedia.rawtherapee.com/Sidecar_Files_-_Processing_Profiles) had
it enabled, the results in 4.1 will be a little different and may
require tuning your old profiles. We tried to preserve
backwards-compatibility where possible, but it was not possible to do
that everywhere. This should not be a problem, because should you
require an identical result you can simply keep using the old version of
RawTherapee and use the new one for future work, and, more importantly,
your skills and taste have evolved over time, so why would you want the
exact same results you had years ago when you can do better now?


**Package maintainers** are please asked to make their builds use a new,
empty [*cache* and *config*](http://rawpedia.rawtherapee.com/File_Paths)
folder with a "4.1" suffix by setting the following *cmake* option:


```
\-DCACHE\_NAME\_SUFFIX="4.1"
```


The reasons for this are as follows:


  - Some users have not checked Preferences in a long time, and their
    program is tuned for what worked best long ago, not for what works
    best now. Our defaults are good ones, we keep them up to date to
    make RawTherapee look and function well out-of-the-box, so having
    4.1 start with fresh defaults is a good thing, and it will motivate
    users to look into Preferences again.
  - Some users have never looked inside Preferences and are not aware of
    some of the features that can be unlocked there. As above, fresh
    defaults will activate these things.
  - Some old *cache* and *config* files can cause RawTherapee to crash.
    While we have patched the specific cases made known to us, it is
    safe to assume there are still cases unknown to us which will still
    cause instability. Starting with clean *cache* and *config* folders
    mitigates this problem.


If possible, inform users where they can find the old *cache* and
*config* folders. Your installation script should not remove these old
folders without asking for the user's informed and explicit consent.


Stay tuned, RawTherapee-4.1 is almost done baking and will be out of the
oven very soon\!

