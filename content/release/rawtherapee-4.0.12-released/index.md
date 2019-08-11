---
title: "RawTherapee 4.0.12 released"
date: 2014-01-07T14:59:00+00:00
author: DrSlony
Tags:
- Downloads
- Versions
---


# RawTherapee 4.0.12 is out\!

Develop your New Year's shots with RawTherapee version 4.0.12\! There
are many new tools to discover and a whole bunch of speed improvements
and bug fixes. There are also changes for builders and package
maintainers, so be sure to read the article\!

Builds should be ready within a day or two. Once they are, get them from
the [Downloads](/downloads) section or using your operating system's
package manager.

We now host our own source code tarballs, get them
from [rawtherapee.com/shared/source](http://rawtherapee.com/shared/source/ "rawtherapee source code repository")

Read below to find out more about what's new.

# New features

* Graduated Filter
* Post-crop Vignette Filter
* Powerful Black-and-White tool
* New curves:
    - Luminance according to hue (LH)
    - Chromaticity according to hue (CH) 
    - Hue according to hue (HH)
    - Chromaticity according to luminance (CL)
* Contrast by Detail Levels tool (wavelet decompose) now has 5 levels
* Auto Levels improved
* Image dimensions added to (i) info
* White Balance slider non-linear for easier control of low and high values
* Noise Reduction tool allows targetting of specific colors (e.g. remove yellow blotches)
* Pre-demosaic automatic removal of chromatic aberration improved
* New output queue template variables %s(0-9)
* New File Browser shortcuts, revision of existing shortcuts (refer to RawPedia)
* New Custom Profile Builder parameters
* Bundled and user profiles in separate submenus
* camconst.json for immediate addition or correction of raw file format support
    - White and black levels
    - Color matrix
    - Crop coordinates
* dcraw 9.19
* The main histogram now shows color levels using the Output Profile
* Enhanced lens info and filter possibilities for manual Nikon lenses
* Added support for
    - Kodak DCS 760 and 760s
    - Various medium-format backs
New DCP profiles for
    - Canon PowerShot S110
    - Fujifilm FinePix S9500
    - Pentax K-5
    - Pentax K-5 II
    - Pentax K-r
* Support for Capture One ICC profiles
* All Bundled Processing Profiles (PP3) revised

\+ Very significant speed improvements and bug fixes.

Refer
to [RawPedia](http://rawpedia.rawtherapee.com/ "RawPedia, the RawTherapee wiki"),
the RawTherapee wiki, for information about these tools and how to use
them.

# Caveats

* Ctrl+q / Ctrl+b  
As of this version, Ctrl+q is used to (q)uit RawTherapee and Ctrl+b is
used to send the currently open image in the Editor tab to the (b)atch
Queue. In the past Ctrl+q was used to send the image to the Batch Queue,
but Ctrl+q is a widely used shortcut to close the application, so we
adopted that convention.

* Memory requirements  
Please read http://rawtherapee.com/blog/maximizing-memory-efficiency

RawTherapee 4.0.12 should be considered a release candidate for version
4.1. That will be our first officially stable version, and we will
release it later this month if no major issues are found with 4.0.12.

* For people compiling RawTherapee  
Build-time requirements:
    - GCC-4.7 or newer is recommended as older versions in some cases can
    lead to artifacts.
    - GTK+ \>=2.24.18 is recommended, as the FileChooserButton in older
    versions of GTK+ is buggy (issue 1852).
* For package maintainers:  
The RawTherapee Manual will not be bundled with further RawTherapee
releases. All documentation is now entered
into [RawPedia](http://rawpedia.rawtherapee.com/ "RawPedia, the RawTherapee wiki"),
the RawTherapee wiki. RawTherapee installers and build scripts should
link to RawPedia, not to the obsolete PDF manual.
