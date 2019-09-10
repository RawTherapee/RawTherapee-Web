---
title: "RawTherapee 5.3 Released"
date: 2017-09-30T22:05:00+00:00
author: DrSlony
draft: false
version: ""
linux_binary: ""
windows_binary: "https://rawtherapee.com/shared/builds/windows/RawTherapee_5.3_WinVista_64.zip"
mac_binary: "https://rawtherapee.com/shared/builds/mac/RawTherapee_OSX_10.9_64_5.3.zip"
source_code: ""
---



RawTherapee 5.3 has been released\!


{{< figure src="rt_splash_5.3.png" >}}


RawTherapee provides you with a selection of powerful tools with which
you can practise the art of developing raw photos. Be sure to read
[RawPedia](http://rawpedia.rawtherapee.com/) to understand how each tool
works so that you may make the most of it. A great place to start is the
"[Getting Started](http://rawpedia.pixls.us/Getting_Started)" article.
Click on "[Main page](http://rawpedia.rawtherapee.com/Main_Page)" in the
top-left corner when you have finished reading that article to see all
other articles.


If you found a problem, don't keep it to yourself. Find out [how to
write useful bug
reports](http://rawpedia.pixls.us/How_to_write_useful_bug_reports) to
get the problem fixed.


Talk with other users and developers in our shared
[forum](https://discuss.pixls.us/c/software/rawtherapee). You can also
have a live chat using [IRC](http://rawpedia.rawtherapee.com/IRC) - no
installation necessary.


Stay informed by following us on
[Google+](https://plus.google.com/+rawtherapee/)


# Download

  - A Windows installer is available from our [Downloads](downloads)
    page.
  - A macOS disk image is available from our [Downloads](downloads)
    page.
  - Linux users can get RawTherapee from their package managers.
  - Compiling yourself? Grab a no-git-required
    [tarball](http://rawtherapee.com/shared/source/) or `git
    checkout 5.3`, then read the
    [Compiling](http://rawpedia.rawtherapee.com/Main_Page#Compiling)
    section in RawPedia.


# News Relevant to Photographers


RawTherapee supports most raw formats, including Pentax Pixel Shift,
Canon Dual-Pixel, and those from Foveon and X-Trans sensors.


If you're wondering whether it supports your camera's raw format, first
download RawTherapee and try for yourself. If a raw format is not
supported it will either not open, or the preview in the Editor tab will
appear black, white, or have a strong color cast - usually magenta. In
that case, read the "[Adding Support for New Raw
Formats](http://rawpedia.rawtherapee.com/Adding_Support_for_New_Raw_Formats)"
in RawPedia.


## In order to use RawTherapee efficiently you should know that:

  - You can scroll all panels using the mouse scroll-wheel.
  - You can right-click on a tool's name to automatically expand it
    while collapsing all others.
  - To change slider values or drop-down list items with the mouse
    scroll-wheel, hold the Shift key. This is so that you can safely
    scroll the panels without accidentally changing a slider or other
    tool setting.
  - All curves support the Shift and Ctrl keys while dragging a point.
    Shift+drag makes the point snap to meaningful axes (top, bottom,
    diagonal, other), while Ctrl+drag makes your mouse movement
    super-fine for precise point positioning.
  - There are many keyboard shortcuts which make working with
    RawTherapee much faster and give you greater control. Make sure you
    familiarize yourself with them on RawPedia's [Keyboard
    Shortcuts](http://rawpedia.rawtherapee.com/Keyboard_Shortcuts)
    page\!

## New Features since 5.2:

  - CIECAM02 enhanced with control over the scene and viewing
    conditions.
  - CIECAM02-friendly "Average Surround" color theme and L\* middle gray
    preview background color, takes into account human vision and color
    appearance with regard to the surrounding color.
  - Manually save the collapsed/expanded state of tools.
  - Lensfun support, for automatic (and manual) profiled lens
    correction.
  - ACES, DCI-P3 Theater and DCI-P3 D65 output color profiles.
  - Numerous speed optimizations and bug fixes.


# News Relevant to Package Maintainers

In general:

  - Requires GTK+ version \>=3.16, though 3.22 is recommended.
  - RawTherapee 5 requires GCC-4.9 or higher, or Clang.
  - Do not use `-ffast-math`, it will not make RawTherapee faster but
    will introduce artifacts.
  - Use `-O3`, it will make RawTherapee faster with no known
    side-effects.
  - For stable releases use `-DCACHE_NAME_SUFFIX=""`
  - For development builds and release-candidates use
    `-DCACHE_NAME_SUFFIX="5-dev"`

## News Relevant to Package Maintainers

Changes since 5.2:

  - Lensfun is required. To use the system-wide lensfun database, do not
    set the CMake option `-DLENSFUNDBDIR`. To use a custom lensfun
    database, set `-DLENSFUNDBDIR="path/to/database"`. See the
    compilation instructions in
    [RawPedia](http://rawpedia.rawtherapee.com/Main_Page#Compiling) for
    more information.


# News Relevant to Developers

  - Announce and discuss your plans in GitHub before starting work.
  - Keep branches small so that completed and working features can be
    merged into the "dev" branch often, and so that they can be
    abandoned if they head in the wrong direction.
  - Use C++11


Complete revision history available on
[GitHub](https://github.com/Beep6581/RawTherapee/commits/5.3).
