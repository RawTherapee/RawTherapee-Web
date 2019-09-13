---
title: "RawTherapee v5.0-r1"
date: 2017-02-02T22:49:00+00:00
author: DrSlony
draft: false
version: "5.0-r1"
linux_appimage: ""
linux_binary_32: ""
linux_binary_64: ""
windows_binary: "https://rawtherapee.com/shared/builds/windows/RawTherapee_5.0-r1-gtk3_WinVista_64.zip"
windows_xp_binary: "https://rawtherapee.com/shared/builds/windows/RawTherapee_5.0-r1-gtk2_WinXP_32.zip"
mac_binary: "https://rawtherapee.com/shared/builds/mac/RawTherapee_OSX_10.9_64_5.0-r1.zip"
source_code: "https://rawtherapee.com/shared/source/rawtherapee-5.0-r1-gtk2.tar.xz"
---

We just released RawTherapee 5.0-r1 which is a revision to the previous release. It addresses some issues which came to light after we made the 5.0 release. Functionally the program is the same -there are no new features - but a few bugs are fixed and we recommend all users upgrade.

The fixes include a correction to the version number used by RawTherapee which is stored in the sidecar files and used by the installer (now the installer will not force an overwrite of your previous installation), it adds back a missing theme when using GTK+ <=3.18,prevents a freeze in the File Browser in Windows, and fixes a compilation problem when using GCC 7.

RawTherapee 5.0 builds have been removed from the Downloads page and 5.0-r1 builds will appear within a day or two.

The source code is available from git by checking out the relevant tag:

* `git checkout 5.0-r1-gtk2`
* `git checkout 5.0-r1-gtk3`
