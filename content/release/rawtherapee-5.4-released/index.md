---
title: "RawTherapee 5.4 Released"
date: 2018-03-20T13:34:00+00:00
author: DrSlony
draft: false
version: ""
linux_binary: ""
windows_binary: ""
mac_binary: ""
source_code: ""
---



RawTherapee 5.4 has been released\!


{{< figure src="rt_splash_5.4.png" >}}


RawTherapee provides you with a selection of powerful tools with which
you can practise the art of developing raw photos. Be sure to read
[RawPedia](http://rawpedia.rawtherapee.com/) to understand how each tool
works so that you may make the most of it. A great place to start is the
"[Getting Started](http://rawpedia.pixls.us/Getting_Started)" article.
Click on "[Main page](http://rawpedia.rawtherapee.com/Main_Page)" in the
top-left corner when you have finished reading that article to see all
other articles.


If you find a problem, don't keep it to yourself. Find out [how to write
useful bug
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
  - Linux users can get RawTherapee from their package managers, or get
    the AppImage from our [Downloads](downloads) page.
  - Compiling yourself? Grab a no-git-required
    [tarball](http://rawtherapee.com/shared/source/) or `git
    checkout 5.4`, then read the
    [Compiling](http://rawpedia.rawtherapee.com/Main_Page#Compiling)
    section in RawPedia.


# News Relevant to Photographers


RawTherapee supports most raw formats, including Pentax and Sony Pixel
Shift, Canon Dual-Pixel, and those from Foveon and X-Trans sensors. If
you're wondering whether it supports your camera's raw format, first
download RawTherapee and try for yourself. If a raw format is not
supported it will either not open, or the preview in the Editor tab will
appear black, white, or have a strong color cast - usually magenta. In
that case, read the "[Adding Support for New Raw
Formats](http://rawpedia.rawtherapee.com/Adding_Support_for_New_Raw_Formats)"
RawPedia article.


## In order to use RawTherapee efficiently you should know that:

  - You can scroll all panels using the mouse scroll-wheel.
  - You can right-click on a tool's name to automatically expand it
    while collapsing all others.
  - To change slider values or drop-down list items with the mouse
    scroll-wheel, hold the Shift key. This is so that you can safely
    scroll the panels without accidentally changing a slider or other
    tool setting.
  - All curves support the Shift and Ctrl keys while dragging a point.
    Shift+drag makes the point snap to a meaningful axis (top, bottom,
    diagonal, other), while Ctrl+drag makes your mouse movement
    super-fine for precise point positioning.
  - There are many keyboard shortcuts which make working with
    RawTherapee much faster and give you greater control. Make sure you
    familiarize yourself with them on RawPedia's "[Keyboard
    Shortcuts](http://rawpedia.rawtherapee.com/Keyboard_Shortcuts)"
    page\!

## Screenshots

See screenshots of RawTherapee 5.4 on our
[Screenshots](http://rawtherapee.com/blog/screenshots) page.

## New Features since 5.3:

  - New default processing profiles, now the default look for raw photos
    closely matches the out-of-camera look with regard to tones and
    includes lens distortion and vignetting correction.
  - New histogram matching tool, to have RawTherapee automatically
    adjust the image for you to match the out-of-camera look with a
    single click of a button.
  - New HDR Tone Mapping tool to compress the light in scenes with a
    high dynamic range, allowing you to show details in both shadows and
    highlights in a realistic way.
  - New Local Contrast tool to boost clarity using a simple interface.
  - New color toning method L\*a\*b\* Color Correction Grid.
  - New RCD demosaicing algorithm to minimize artifacts even with
    artificial lighting and strong chromatic aberration.
  - New thumbnail overlay icons in the File Browser and Filmstrip to
    help you distinguish normal images from HDR and Pixel Shift ones.
  - Added support for showing out-of-gamut areas based on the output
    profile.
  - Added support for reading and writing metadata and ICC profiles to
    and from PNG images.
  - Added support for processing Sony Pixel Shift ARQ raw files - make
    sure that the ARQ extension is enabled in Preferences \> File
    Browser \> Parsed Extensions.
  - Create Sony ARQ raw files using
    https://github.com/agriggio/make\_arq
  - Added support for saving 32-bit floating-point TIFFs clamped to
    \[0;1\].
  - Added profiled chromatic aberration correction support using
    Lensfun.
  - More tools now have an on/off switch.
  - The user interface is cleaner, with all power-house tools moved into
    a new "Advanced" tab to prevent slider-shock to newcomers.
  - The Metadata tab now lets you choose whether you want to copy
    metadata unchanged, edit metadata or strip metadata when saving
    images. Now you can also make metadata changes in batch mode.
  - The choice of whether the main histogram should display information
    using the working profile or the output profile is now available
    from the Editor tab's top toolbar.
  - The Crop tool's aspect ratio now defaults to that of the image, and
    RawTherapee automatically zooms-to-fit the crop once it's placed.
  - RGB input-type ICC profiles can now be used as output profiles.
  - The saved reference image for profiling (created from within the
    Color Management tool) now contains metadata.
  - PNG and compressed TIFF images make use of better compression.
  - Shortcut key changes: Zoom-to-fit the crop using "f", fit the whole
    image using "Alt+f".

There were several hundred commits optimizing processing speed and
memory usage as well as bug fixes and code refactoring, though the
details of these are too arcane to list here. The effort involved
thousands of developer-hours.

RawTherapee and other open-source projects require access to sample raw
files from various camera makes and models in order to support those raw
formats correctly. You can help by submitting raw files to RPU:
<https://raw.pixls.us/>


# News Relevant to Package Maintainers

No changes since 5.3.

  - To get the source code, either clone from git or use the tarball
    from <http://rawtherapee.com/shared/source/> . Do not use the
    auto-generated GitHub release tarballs.
  - Requires GTK+ version \>=3.16, though \>=3.22 is recommended.
  - RawTherapee 5 requires GCC-4.9 or higher, or Clang.
  - Do not use `-ffast-math`, it will not make RawTherapee faster but
    will introduce artifacts.
  - Use `-O3`, it will make RawTherapee faster with no known
    side-effects.
  - For stable releases use `-DCACHE_NAME_SUFFIX=""`
  - For development builds and release-candidates use
    `-DCACHE_NAME_SUFFIX="5-dev"`


# News Relevant to Developers

See
[CONTRIBUTING.md](https://github.com/Beep6581/RawTherapee/blob/dev/CONTRIBUTING.md).


Complete revision history available on
[GitHub](https://github.com/Beep6581/RawTherapee/commits/5.4).
