---
title: "RawTherapee v5.3"
date: 2017-09-30T22:05:00+00:00
author: DrSlony
draft: false
version: ""
linux_appimage: ""
linux_binary_32: ""
linux_binary_64: ""
windows_binary: "https://rawtherapee.com/shared/builds/windows/RawTherapee_5.3_WinVista_64.zip"
windows_xp_binary: ""
mac_binary: "https://rawtherapee.com/shared/builds/mac/RawTherapee_OSX_10.9_64_5.3.zip"
source_code: "https://rawtherapee.com/shared/source/rawtherapee-5.3.tar.xz"
---


RawTherapee 5.3 has been released\!

{{< figure src="rt_splash_5.3.png" >}}

## New Features

- CIECAM02 enhanced with control over the scene and viewing conditions.
- CIECAM02-friendly "Average Surround" color theme and L\- middle gray preview background color, takes into account human vision and color appearance with regard to the surrounding color.
- Manually save the collapsed/expanded state of tools.
- Lensfun support, for automatic (and manual) profiled lens correction.
- ACES, DCI-P3 Theater and DCI-P3 D65 output color profiles.
- Numerous speed optimizations and bug fixes.


## News Relevant to Package Maintainers

In general:

- Requires GTK+ version \>=3.16, though 3.22 is recommended.
- RawTherapee 5 requires GCC-4.9 or higher, or Clang.
- Do not use `-ffast-math`, it will not make RawTherapee faster but will introduce artifacts.
- Use `-O3`, it will make RawTherapee faster with no known side-effects.
- For stable releases use `-DCACHE_NAME_SUFFIX=""`
- For development builds and release-candidates use `-DCACHE_NAME_SUFFIX="5-dev"`

## News Relevant to Package Maintainers

Changes since 5.2:

- Lensfun is required. To use the system-wide lensfun database, do not set the CMake option `-DLENSFUNDBDIR`. To use a custom lensfun database, set `-DLENSFUNDBDIR="path/to/database"`. See the compilation instructions in [RawPedia](http://rawpedia.rawtherapee.com/Main_Page#Compiling) for more information.


## News Relevant to Developers

- Announce and discuss your plans in GitHub before starting work.
- Keep branches small so that completed and working features can be merged into the "dev" branch often, and so that they can be abandoned if they head in the wrong direction.
- Use C++11


Complete revision history available on
[GitHub](https://github.com/Beep6581/RawTherapee/commits/5.3).
