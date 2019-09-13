---
title: "RawTherapee version 5.6"
date: 2019-04-20T22:22:12+02:00
draft: false
version: "5.6"
linux_binary: "https://rawtherapee.com/shared/builds/linux/RawTherapee-releases-5.6-20190420.AppImage"
windows_binary: "https://rawtherapee.com/shared/builds/windows/RawTherapee_5.6_WinVista_64.zip"
mac_binary: "https://rawtherapee.com/shared/builds/mac/RawTherapee_OSX_10.9_64_5.6.zip"
source_code: "http://rawtherapee.com/shared/source/"
---

RawTherapee provides you with a selection of powerful tools with which you can practise the art of developing raw photos. Be sure to read [RawPedia][] to understand how each tool works so that you may make the most of it. A great place to start is the "[Getting Started][]" article. Click on "[Main page][]" in the top-left corner when you have finished reading that article to see all other articles.

If you find a problem, don't keep it to yourself. Find out [how to write useful bug reports][] to get the problem fixed.

Talk with other users and developers in our shared [forum][]. You can also have a live chat using [IRC][] - no installation necessary.

[RawPedia]: http://rawpedia.rawtherapee.com/
[Getting Started]: http://rawpedia.pixls.us/Getting_Started
[Main page]: http://rawpedia.rawtherapee.com/Main_Page
[how to write useful bug reports]: http://rawpedia.rawtherapee.com/How_to_write_useful_bug_reports
[forum]: https://discuss.pixls.us/c/software/rawtherapee
[IRC]: http://rawpedia.rawtherapee.com/IRC

## Download

* A Windows installer is available from our [Downloads][] page.
* A macOS disk image is available from our [Downloads][] page.
* Linux users can get RawTherapee from their package managers, or get the AppImage from our [Downloads][] page.
* Compiling yourself? Grab a no-git-required [tarball](http://rawtherapee.com/shared/source/) or `git checkout 5.6`, then read the [Compiling][] section in RawPedia.

[Downloads]: /downloads/
[Compiling]: http://rawpedia.rawtherapee.com/Main_Page#Compiling

## News Relevant to Photographers
RawTherapee supports most raw formats, including Pentax and Sony Pixel Shift, Canon Dual-Pixel, and those from Foveon and X-Trans sensors. If you're wondering whether it supports your camera's raw format, first download RawTherapee and try for yourself. If a raw format is not supported it will either not open, or the preview in the Editor tab will appear black, white, or have a strong color cast - usually magenta. In that case, read the "[Adding Support for New Raw Formats][]" RawPedia article.

[Adding Support for New Raw Formats]: http://rawpedia.rawtherapee.com/Adding_Support_for_New_Raw_Formats


## In order to use RawTherapee efficiently you should know that:

* You can scroll all panels using the mouse scroll-wheel.
* You can right-click on a tool's name to automatically expand it while collapsing all others.
* To change slider values or drop-down list items with the mouse scroll-wheel, hold the Shift key. This is so that you can safely scroll the panels without accidentally changing a slider or other tool setting.
* All curves support the Shift and Ctrl keys while dragging a point. Shift+drag makes the point snap to a meaningful axis (top, bottom, diagonal, other), while Ctrl+drag makes your mouse movement super-fine for precise point positioning.
* There are many keyboard shortcuts which make working with RawTherapee much faster and give you greater control. Make sure you familiarize yourself with them on RawPedia's "Keyboard Shortcuts" page!


## New Features since 5.5:

* Pseudo-HiDPI support, for a smooth and sharp user interface regardless of screen size. Pseudo-HiDPI mode is disabled by default, enable it in Preferences > General > Appearance. Scaling in RawTherapee depends on font size, DPI and display scaling. While scaling has been tested to work well in Windows, Linux and macOS, there are some macOS display modes which are incompatible with it, specifically those modes suffixed by "(HiDPI)" in macOS Display settings. Some versions of macOS (10.14.*) seem to not list any modes, in which case the user must just give it a try.
* Ability to move tools to a new Favorites tab.
* "Unclipped" processing profile, to make it easy to save an image while preserving data across the whole tonal range.
* User-adjustable tiles-per-thread settings in Preferences > Performance, for users who want to find optimal values for their system. The default value of 2 tiles-per-thread performs best overall.
* Hundreds of speed optimizations, bug fixes, and overall improvements.

RawTherapee and other open-source projects require access to sample raw files from various camera makes and models in order to support those raw formats correctly. You can help by submitting raw files to RPU: https://raw.pixls.us/

## News Relevant to Package Maintainers

Changes since 5.5:

* Requires librsvg >= 2.40.
* GTK+ versions 3.24.2 - 3.24.6 have an issue where combobox menu scroll-arrows are missing when the combobox list does not fit vertically on the screen. As a result, users would not be able to scroll in the following comboboxes: Processing Profiles, Film Simulation, and the camera and lens profiles in Profiled Lens Correction.

In general:

* To get the source code, either clone from git or use the tarball from http://rawtherapee.com/shared/source/ . Do not use the auto-generated GitHub release tarballs.
* Requires GTK+ version >=3.16, though >=3.22.24 is recommended.
* RawTherapee 5 requires GCC-4.9 or higher, or Clang.
* Do not use -ffast-math, it will not make RawTherapee faster but will introduce artifacts.
* Use -O3, it will make RawTherapee faster with no known side-effects.
* For stable releases use -DCACHE_NAME_SUFFIX=""
* For development builds and release-candidates use -DCACHE_NAME_SUFFIX="5-dev"


## News Relevant to Developers

See [CONTRIBUTING.md](https://github.com/Beep6581/RawTherapee/blob/dev/CONTRIBUTING.md).

Complete revision history [available on GitHub](https://github.com/Beep6581/RawTherapee/commits/5.6).
