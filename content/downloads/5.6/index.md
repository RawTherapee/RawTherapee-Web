---
title: "RawTherapee v5.6"
date: 2019-04-20T22:22:12+02:00
draft: false
version: "5.6"
linux_appimage: "https://rawtherapee.com/shared/builds/linux/RawTherapee-releases-5.6-20190420.AppImage"
linux_binary_32: ""
linux_binary_64: ""
windows_binary: "https://rawtherapee.com/shared/builds/windows/RawTherapee_5.6_WinVista_64.zip"
windows_xp_binary: ""
mac_binary: "https://rawtherapee.com/shared/builds/mac/RawTherapee_OSX_10.9_64_5.6.zip"
source_code: "https://rawtherapee.com/shared/source/rawtherapee-5.6.tar.xz"
---

## New Features

- Pseudo-HiDPI support, for a smooth and sharp user interface regardless of screen size. Pseudo-HiDPI mode is disabled by default, enable it in Preferences > General > Appearance. Scaling in RawTherapee depends on font size, DPI and display scaling. While scaling has been tested to work well in Windows, Linux and macOS, there are some macOS display modes which are incompatible with it, specifically those modes suffixed by "(HiDPI)" in macOS Display settings. Some versions of macOS (10.14.*) seem to not list any modes, in which case the user must just give it a try.
- Ability to move tools to a new Favorites tab.
- "Unclipped" processing profile, to make it easy to save an image while preserving data across the whole tonal range.
- User-adjustable tiles-per-thread settings in Preferences > Performance, for users who want to find optimal values for their system. The default value of 2 tiles-per-thread performs best overall.
- Hundreds of speed optimizations, bug fixes, and overall improvements.

RawTherapee and other open-source projects require access to sample raw files from various camera makes and models in order to support those raw formats correctly. You can help by submitting raw files to RPU: https://raw.pixls.us/

## News Relevant to Package Maintainers

Changes since 5.5:

- Requires librsvg >= 2.40.
- GTK+ versions 3.24.2 - 3.24.6 have an issue where combobox menu scroll-arrows are missing when the combobox list does not fit vertically on the screen. As a result, users would not be able to scroll in the following comboboxes: Processing Profiles, Film Simulation, and the camera and lens profiles in Profiled Lens Correction.

In general:

- To get the source code, either clone from git or use the tarball from http://rawtherapee.com/shared/source/ . Do not use the auto-generated GitHub release tarballs.
- Requires GTK+ version >=3.16, though >=3.22.24 is recommended.
- RawTherapee 5 requires GCC-4.9 or higher, or Clang.
- Do not use `-ffast-math`, it will not make RawTherapee faster but will introduce artifacts.
- Use `-O3`, it will make RawTherapee faster with no known side-effects.
- For stable releases use `-DCACHE_NAME_SUFFIX=""`
- For development builds and release-candidates use `-DCACHE_NAME_SUFFIX="5-dev"`


## News Relevant to Developers

See [CONTRIBUTING.md](https://github.com/Beep6581/RawTherapee/blob/dev/CONTRIBUTING.md).

Complete revision history [available on GitHub](https://github.com/Beep6581/RawTherapee/commits/5.6).
