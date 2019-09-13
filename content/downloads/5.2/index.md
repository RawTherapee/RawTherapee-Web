---
title: "RawTherapee v5.2"
date: 2017-07-23T23:23:00+00:00
author: DrSlony
draft: false
version: "5.2"
linux_appimage: ""
linux_binary_32: ""
linux_binary_64: ""
windows_binary: "https://rawtherapee.com/shared/builds/windows/RawTherapee_5.2_WinVista_64.zip"
windows_xp_binary: ""
mac_binary: "https://rawtherapee.com/shared/builds/mac/RawTherapee_OSX_10.9_64_5.2.zip"
source_code: "https://rawtherapee.com/shared/source/rawtherapee-5.2.tar.xz"
---


RawTherapee 5.2 has been unleashed\!

{{< figure src="rt_splash_5.2.png" >}}

## New Features

- GIMP plugin to open raw images in GIMP using RawTherapee - see [RawPedia](http://rawpedia.rawtherapee.com/GIMP_Plugin).
- "Remote" mode (-R command line option) to allow opening images ("Open with" or passed as arguments) in a full-fledged instance. The -R mode allows you to open an image in an already-running instance of RawTherapee, if that instance was also started using -R. Opening an image without the -R option will open RawTherapee in "no-File-Browser" mode which lacks the File Browser and Queue tabs, and the Preferences button.
- Added DCP profiles for accurate color for:
  - FUJIFILM X-T20

While this release introduced several new features, the main focus was to refine what's already there. Both the speed and stability of various tools and of RawTherapee in general were significantly improved, particularly when dealing with folders containing thousands of images.

## Most significant improvements:

- 4x speedup of the Microcontrast tool.
- CIECAM02 curves no longer cause a sudden jump in brightness.
- Improved stability in METM (Multiple Editor Tabs Mode) in Windows.
- Improvement to the MEOW (Multiple Editor Tabs in Own Window) mode.
- LCP files lead to better results.
- Large speedup and stability improvement when opening folders containing hundreds or thousands of images.
- Many memory leaks fixed.
- Pixel Shift speedups, reduction of memory requirements, and motion mask preview accuracy improved.
- The preview of the Tone Mapping tool is now much more accurate at any zoom level.


## News Relevant to Package Maintainers

In general:

- Requires GTK+ version \>=3.16, though 3.22 is recommended.
- RawTherapee 5 requires GCC-4.9 or higher, or Clang.
- Do not use `-ffast-math`, it will not make RawTherapee faster but will introduce artifacts.
- Use `-O3`, it will make RawTherapee faster with no known side-effects.
- For stable releases use `-DCACHE_NAME_SUFFIX=""`
- For development builds and release-candidates use `-DCACHE_NAME_SUFFIX="5-dev"`

## News Relevant to Package Maintainers

Changes since 5.1:

- BZIP2 support removed - no more BZIP2 dependency.
- Added possibility to use system KLT library if available, otherwise our shipped version is used.


## News Relevant to Developers

- Announce and discuss your plans in GitHub before starting work.
- Keep branches small so that completed and working features can be merged into the "dev" branch often, and so that they can be abandoned if they head in the wrong direction.
- Use C++11
- Code must be run through astyle.

Complete revision history available on
[GitHub](https://github.com/Beep6581/RawTherapee/commits/5.2).
