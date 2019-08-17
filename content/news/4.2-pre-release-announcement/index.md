---
title: "4.2 Pre-Release Announcement"
date: 2014-10-21T17:46:00+00:00
author: DrSlony
Tags:
- Versions
---


<div id="article_show_text">

Dear **package
maintainers**\! <span style="line-height: 25.6000003814697px;">We will
be releasing RawTherapee-4.2 this Friday, 2014-10-24. Please take a
minute to read this announcement.</span>



Please
make your builds use [*cache* and
*config*](http://rawpedia.rawtherapee.com/File_Paths)<span style="line-height: 25.6000003814697px;">
folders called just "RawTherapee" without any version suffix. This can
be done by setting the following
option:


```
\-DCACHE\_NAME\_SUFFIX=""
```


In the past we requested that a clean cache and config folder is created
by appending the RawTherapee version. We hope that that move has
accomplished its purpose, and now strive to offer a seamless and stable
upgrade process to users by re-using these files.


See [issue 2427](https://code.google.com/p/rawtherapee/issues/detail?id=2427) for
a discussion.


You may optionally want to make the installer check for the existence of
any RawTherapee cache and config folder, and, if one is found, inform
the user that they can simply copy over the contents from e.g.
\~/.config/RawTherapee-4.1 to \~/.config/RawTherapee


At the same time it would be good to point them
to [RawPedia](http://rawpedia.rawtherapee.com/ "RawPedia") so they can
find out how to fix crashes on startup and how to write useful bug
reports.


We will also be shipping a *rawtherapee.appdata.xml* file. See
the [freedesktop.org AppData
page](http://people.freedesktop.org/~hughsient/appdata/ "freedesktop.org AppData"),
and [issue
2512](https://code.google.com/p/rawtherapee/issues/detail?id=2512 "Issue 2512 on Google Code").
Do with it as you will\!

