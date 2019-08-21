---
title: "RawTherapee 5.1 released"
date: 2017-05-15T22:06:00+00:00
author: DrSlony
draft: false
version: ""
linux_binary: ""
windows_binary: "https://rawtherapee.com/releases_head/windows/RawTherapee_5.1_WinVista_64.zip"
mac_binary: "https://rawtherapee.com/releases_head/mac/RawTherapee_OSX_10.9_64_5.1.zip"
source_code: ""
---



We entered the woods in the dead of night, we followed the scream of the
owls, they led us to a fireside, we stood in a circle, our beards hung
low and we chanted, and we hummed, and we swayed to and fro, and we
concluded that we are unquestionably thrilled to release RawTherapee
5.1\!


{{< figure src="rt_splash_5.1.png" >}}


RawTherapee provides you with a selection of powerful tools with which
you can practice the art of developing raw photos. Be sure to read
[RawPedia](http://rawpedia.rawtherapee.com/) to understand how each tool
works so that you may make the most of it. A great place to start is the
"[Getting Started](http://rawpedia.pixls.us/Getting_Started)" article.
Click on "[Main page](http://rawpedia.rawtherapee.com/Main_Page)" in the
top-left corner when you have finished reading that article to see all
other articles.


If you found a problem, don't keep it to yourself. Find out [how to write useful bug reports](http://rawpedia.pixls.us/How_to_write_useful_bug_reports) to
get the problem fixed.


Talk with other users and developers in our shared
[forum](https://discuss.pixls.us/c/software/rawtherapee). You can also
have a live chat using [IRC](http://rawpedia.rawtherapee.com/IRC) - no
installation necessary.


Stay informed by following us on
[Google+](https://plus.google.com/+rawtherapee/)


# Download

  - Windows installers and macOS builds are available from our
    [Downloads](downloads) page.
  - Linux users can get RawTherapee from their package managers.
  - Compiling yourself? Grab a no-git-required
    [tarball](http://rawtherapee.com/shared/source/) or `git
    checkout 5.1`, then read the
    [Compiling](http://rawpedia.rawtherapee.com/Main_Page#Compiling)
    section in RawPedia.


# News Relevant to Photographers


RawTherapee 5.1 supports most raw formats, including some unusual ones
like those from cameras using Foveon and X-Trans sensors. If you're
wondering whether it supports your camera's raw format, first download
RawTherapee 5.1 and try for yourself. If a raw format is not supported
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

## New Features

  - Pentax Pixel Shift support, to automatically combine sub-images from
    a Pentax Pixel Shift raw file into one high quality image, with
    support for automatic motion detection and masking.
  - Support for processing any sub-image from raw formats which support
    multiple images. Currently up to 4 sub-images supported.
  - Dynamic Profile Creator to automatically generate per-image custom
    processing profiles by merging existing processing profiles based on
    image metadata (Exif).
  - New command-line executable "rawtherapee-cli(.exe)" to reduce
    startup time for command-line operations.
  - HaldCLUT paths are now relative to the HaldCLUT folder as set in
    Preferences. This enables you to share PP3 files easier.
  - Auto White Balance now has a Temperature Bias, letting you make the
    automatic temperature warmer or cooler.
  - LCP correction works for raw and non-raw files.
  - LCP distortion correction support for fisheye lenses.
  - Certain tools are now hidden or disabled if the loaded image does
    not support them, e.g. the tools in the Raw tab are disabled when
    working with a non-raw file.
  - Improved fit-to-window zoom functionality of the main preview in the
    Editor tab.
  - New Fast Export option to downscale the image before processing, to
    increase speed.
  - Custom crop ratio.
  - Automatic monitor profile detection also in Linux.
  - Lens information support added for Panasonic cameras.
  - Support for lossy DNG files.
  - Support for compressed Fujifilm Bayer raw files.
  - Support for compressed X-Trans raw files.
  - Support for Sigma sd Quattro DNG raw files.
  - Added DCP profiles for accurate color for:
      - FUJIFILM X100S
      - LG Mobile LG-H815 (LG G4)
      - NIKON D300
      - NIKON D300
      - NIKON D5600
      - NIKON D80
      - NIKON D810
      - OLYMPUS E-M1MarkII
      - Panasonic DMC-GX85


# News Relevant to Package Maintainers

  - No significant changes since 5.0-r1.
  - GTK2 is not supported. 5.0-r1 was the last GTK2 release.
  - Branches "master" and "gtk3" are dead, do not use them.
  - RawTherapee 5 requires GCC-4.9 or higher, or Clang.
  - Do not use `-ffast-math`, it will not make RawTherapee faster but
    will introduce artifacts.
  - Use `-O3`, it will make RawTherapee faster with no known
    side-effects.
  - For stable releases use `-DCACHE_NAME_SUFFIX=""`
  - For development builds and release-candidates use
    `-DCACHE_NAME_SUFFIX="5-dev"`


# News Relevant to Developers

  - Announce and discuss your plans in GitHub before starting work.
  - Keep branches small so that completed and working features can be
    merged into the "dev" branch often, and so that they can be
    abandoned if they head in the wrong direction.
  - Use C++11
  - Code must be run through astyle.


Complete revision history available on
[GitHub](https://github.com/Beep6581/RawTherapee/commits/5.1).
