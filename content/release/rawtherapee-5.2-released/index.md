---
title: "RawTherapee 5.2 Released"
date: 2017-07-23T23:23:00+00:00
author: DrSlony
---



RawTherapee 5.2 has been unleashed\!


{{< figure src="rt_splash_5.2.png" >}}


RawTherapee provides you with a selection of powerful tools with which
you can practice the art of developing raw photos. Be sure to read
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

  - A Windows installer and a macOS build are available from our
    [Downloads](downloads) page.
  - Linux users can get RawTherapee from their package managers.
  - Compiling yourself? Grab a no-git-required
    [tarball](http://rawtherapee.com/shared/source/) or `git
    checkout 5.2`, then read the
    [Compiling](http://rawpedia.rawtherapee.com/Main_Page#Compiling)
    section in RawPedia.


# News Relevant to Photographers


RawTherapee 5.2 supports most raw formats, including some unusual ones
like those from cameras using Foveon and X-Trans sensors. If you're
wondering whether it supports your camera's raw format, first download
RawTherapee 5.2 and try for yourself. If a raw format is not supported
it will either not open, or the preview in the Editor tab will appear
black, white, or have a strong color cast - usually magenta. In that
case, read "[Adding Support for New Raw
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

## New Features since 5.1:

* GIMP plugin to open raw images in GIMP using RawTherapee -
see [RawPedia](http://rawpedia.rawtherapee.com/GIMP_Plugin).

* "Remote" mode (-R command line option) to allow opening images ("Open
with" or passed as arguments) in a full-fledged instance. The -R mode
allows you to open an image in an already-running instance of
RawTherapee, if that instance was also started using -R. Opening an
image without the -R option will open RawTherapee in "no-File-Browser"
mode which lacks the File Browser and Queue tabs, and the Preferences
button.

* Added DCP profiles for accurate color for:

  - FUJIFILM X-T20

While this release introduced several new features, the main focus was
to refine what's already there. Both the speed and stability of various
tools and of RawTherapee in general were significantly improved,
particularly when dealing with folders containing thousands of images.

## Most significant improvements:

  - 4x speedup of the Microcontrast tool.
  - CIECAM02 curves no longer cause a sudden jump in brightness.
  - Improved stability in METM (Multiple Editor Tabs Mode) in Windows.
  - Improvement to the MEOW (Multiple Editor Tabs in Own Window) mode.
  - LCP files lead to better results.
  - Large speedup and stability improvement when opening folders
    containing hundreds or thousands of images.
  - Many memory leaks fixed.
  - Pixel Shift speedups, reduction of memory requirements, and motion
    mask preview accuracy improved.
  - The preview of the Tone Mapping tool is now much more accurate at
    any zoom level.


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

Changes since 5.1:

  - BZIP2 support removed - no more BZIP2 dependency.
  - Added possibility to use system KLT library if available, otherwise
    our shipped version is used.


# News Relevant to Developers

  - Announce and discuss your plans in GitHub before starting work.
  - Keep branches small so that completed and working features can be
    merged into the "dev" branch often, and so that they can be
    abandoned if they head in the wrong direction.
  - Use C++11
  - Code must be run through astyle.


Complete revision history available on
[GitHub](https://github.com/Beep6581/RawTherapee/commits/5.2).

