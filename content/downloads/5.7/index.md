---
title: "RawTherapee version 5.7"
date: 2019-09-10T15:39:50+02:00
draft: false
version: "5.7"
linux_binary: "https://rawtherapee.com/shared/builds/linux/RawTherapee-releases-5.7-20190910.AppImage"
windows_binary: "https://rawtherapee.com/shared/builds/windows/RawTherapee_5.7_WinVista_64.zip"
mac_binary: ""
source_code: "https://rawtherapee.com/shared/source/"
---

RawTherapee 5.7 has been released\!

{{< figure src="rt57_drosera_rotundifolia.jpg" >}}

RawTherapee provides you with a selection of powerful tools with which you can practise the art of developing raw photos. Be sure to read [RawPedia][] to understand how each tool works so that you may make the most of it. A great place to start is the "[Getting Started][]" article. Click on "[Main page][]" in the top-left corner when you have finished reading that article to see all other articles.

If you find a problem, don't keep it to yourself. Find out [how to write useful bug reports][] to get the problem fixed.

Talk with other users and developers in our shared [forum][]. You can also have a live chat using [IRC][] - no installation necessary.

[RawPedia]: https://rawpedia.rawtherapee.com/
[Getting Started]: https://rawpedia.pixls.us/Getting_Started
[Main page]: https://rawpedia.rawtherapee.com/Main_Page
[how to write useful bug reports]: https://rawpedia.rawtherapee.com/How_to_write_useful_bug_reports
[forum]: https://discuss.pixls.us/c/software/rawtherapee
[IRC]: https://rawpedia.rawtherapee.com/IRC

## Download

* A Windows installer is available from our [Downloads][] page.
* A macOS disk image is available from our [Downloads][] page.
* Linux users can get RawTherapee from their package managers, or get the AppImage from our [Downloads][] page.
* Compiling yourself? Grab a no-git-required [tarball](https://rawtherapee.com/shared/source/) or `git checkout 5.7`, then read the [Compiling][] section in RawPedia.

[Downloads]: /downloads/
[Compiling]: https://rawpedia.rawtherapee.com/Main_Page#Compiling

## News Relevant to Photographers
RawTherapee supports most raw formats, including Pentax and Sony Pixel Shift, Canon Dual-Pixel, and those from Foveon and X-Trans sensors. If you're wondering whether it supports your camera's raw format, first download RawTherapee and try for yourself. If a raw format is not supported it will either not open, or the preview in the Editor tab will appear black, white, or have a strong color cast - usually magenta. In that case, read the "[Adding Support for New Raw Formats][]" RawPedia article.

[Adding Support for New Raw Formats]: https://rawpedia.rawtherapee.com/Adding_Support_for_New_Raw_Formats


## In order to use RawTherapee efficiently you should know that:

* You can scroll all panels using the mouse scroll-wheel.
* You can right-click on a tool's name to automatically expand it while collapsing all others.
* To change slider values or drop-down list items with the mouse scroll-wheel, hold the Shift key. This is so that you can safely scroll the panels without accidentally changing a slider or other tool setting.
* All curves support the Shift and Ctrl keys while dragging a point. Shift+drag makes the point snap to a meaningful axis (top, bottom, diagonal, other), while Ctrl+drag makes your mouse movement super-fine for precise point positioning.
* There are many keyboard shortcuts which make working with RawTherapee much faster and give you greater control. Make sure you familiarize yourself with them on RawPedia's "Keyboard Shortcuts" page!


## New Features since 5.6:

* Film Negative tool, for easily developing raw photographs of film negatives.
* Support for reading "rating" tags from Exif and XMP, shown in the File Browser/Filmstrip using RawTherapee's star rating system.
* Hundreds of bug fixes, speed optimizations and raw format support improvements.

RawTherapee and other open-source projects require access to sample raw files from various camera makes and models in order to support those raw formats correctly. You can help by submitting raw files to RPU: https://raw.pixls.us/

## News Relevant to Package Maintainers

New since 5.6:

* Requires CMake >=3.5.

In general:

* To get the source code, either clone from git or use the tarball from https://rawtherapee.com/shared/source/ . Do not use the auto-generated GitHub release tarballs.
* Requires GTK+ version >=3.16, though >=3.22.24 is recommended.
* GTK+ versions 3.24.2 - 3.24.6 have an issue where combobox menu scroll-arrows are missing when the combobox list does not fit vertically on the screen. As a result, users would not be able to scroll in the following comboboxes: Processing Profiles, Film Simulation, and the camera and lens profiles in Profiled Lens Correction.
* RawTherapee 5 requires GCC-4.9 or higher, or Clang.
* Do not use `-ffast-math`, it will not make RawTherapee faster but will introduce artifacts.
* Use `-O3`, it will make RawTherapee faster with no known side-effects.
* For stable releases use `-DCACHE_NAME_SUFFIX=""`
* For development builds and release-candidates use `-DCACHE_NAME_SUFFIX="5-dev"`


## News Relevant to Developers

See [CONTRIBUTING.md](https://github.com/Beep6581/RawTherapee/blob/dev/CONTRIBUTING.md).

Complete revision history [available on GitHub](https://github.com/Beep6581/RawTherapee/commits/5.7).
