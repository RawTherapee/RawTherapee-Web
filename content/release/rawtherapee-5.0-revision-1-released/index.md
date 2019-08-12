---
title: "RawTherapee 5.0 Revision 1 Released!"
date: 2017-02-02T22:49:00+00:00
author: DrSlony
---

We just released RawTherapee 5.0-r1 which is a revision to the previous
release. It addresses some issues which came to light after we made the
5.0 release. Functionally the program is the same -there are no new
features - but a few bugs are fixed and we recommend all users upgrade.

The fixes include a correction to the version number used by RawTherapee
which is stored in the sidecar files and used by the installer (now the
installer will not force an overwrite of your previous installation), it
adds back a missing theme when using GTK+ <=3.18,prevents a freeze in
the File Browser in Windows, and fixes a compilation problem when using
GCC 7.

RawTherapee 5.0 builds have been removed from the Downloads page and
5.0-r1 builds will appear within a day or two.

The source code is available from git by checking out the tags
[5.0-r1-gtk2](https://github.com/Beep6581/RawTherapee/releases/tag/5.0-r1-gtk2)
or
[5.0-r1-gtk3](https://github.com/Beep6581/RawTherapee/releases/tag/5.0-r1-gtk3),
or in the form of a [tarball](http://rawtherapee.com/shared/source/).

