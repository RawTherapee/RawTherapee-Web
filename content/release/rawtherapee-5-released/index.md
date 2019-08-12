---
title: "RawTherapee 5 Released!"
date: 2017-01-22T19:46:00+00:00
author: DrSlony
---



We are absolutely thrilled to release RawTherapee 5\!


{{< figure src="rt_splash_5.0.png" >}}


Builds will be available within a day or two. In the meanwhile, keep
reading to find out important things you should be aware of.



{{< figure src="Rt-5-misty1_th.jpg" link="Rt-5-misty1.jpg" >}}


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


# News Relevant to Photographers


RawTherapee 5 supports most raw formats, including some unusual ones
like those from cameras using Foveon and X-Trans sensors. If you're
wondering whether it supports your camera's raw format, first download
RawTherapee 5 and try for yourself. If a raw format is not supported it
will either not open, or the preview in the Editor tab will appear
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

  - [Wavelets tool](http://rawpedia.rawtherapee.com/Wavelets).
  - [Retinex tool](http://rawpedia.rawtherapee.com/Retinex/fr).
  - Monitor profile and rendering intent support.
  - Print soft-proofing support.
  - Automatic chroma noise reduction, manual luminance noise reduction
    using sliders and curves.
  - The "Inspect" tab in the File Browser lets you see a 100% preview of
    the image whose thumbnail your mouse cursor hovers over, which is
    either the largest JPEG image embedded in the raw file or the image
    itself when hovering over non-raw images.
  - The [curve
    pipette](http://rawpedia.rawtherapee.com/General_Comments_About_Some_Toolbox_Widgets#General_Comments_on_Tone_and_Flat_Curves)
    allows you to pick the right point of a curve by clicking in the
    preview, and input/output values so that you can set the desired
    output value for a given input value.
  - [Post-resize
    sharpening](http://rawpedia.rawtherapee.com/Resize#Post-Resize_Sharpening),
    to give your photos that subtle crispness after resizing them.
  - Dual-illuminant
    [DCP](http://rawpedia.rawtherapee.com/How_to_create_DCP_color_profiles#What_are_DCP_profiles_and_why_do_I_need_them.3F)
    support with curves, base tables, look tables and baseline exposure.
  - New exposure [tone curve
    modes](http://rawpedia.rawtherapee.com/Exposure#Curve_Mode)
    "Luminance" and "Perceptual".
  - Queue processing will stop if an error is encountered while saving,
    e.g. if you run out of disk space.
  - The Contrast by Detail Levels tool received the "[Process Locate
    Before/After
    Black-and-White](http://rawpedia.rawtherapee.com/Contrast_by_Detail_Levels#Process_Locate_Before.2FAfter_Black-and-White)"
    option.
  - Rec. 2020 ICC profile added.
  - The Navigator can show RGB, HSV and L\*a\*b\* values in a range of
    0-255, 0-1 or %.
  - The Lockable Color Picker allows you to place multiple sample points
    over the preview to measure colors and see them change in real time
    as you manipulate the image. They support the same ranges as the
    Navigator.
  - Grayscale JPEG and TIFF images are now supported.
  - 32-bit TIFF files are supported.
  - In addition to these new features, RawTherapee received over two
    years worth of amazing speedups, code cleanups and bug fixes, making
    it faster and more stable than ever before\!


# News Relevant to Package Maintainers

  - Build RawTherapee 5.0 using these tarballs:
    [rawtherapee.com/shared/source/](http://rawtherapee.com/shared/source/)
  - Nightly builds from git may compile but not run well, we're working
    on it, see issue
    \#[\#3628](https://github.com/Beep6581/RawTherapee/issues/3628).
  - Branch "master" uses GTK2, branch "gtk3" requires GTK+ \>=3.16.
    There are known bugs using GTK+ versions 3.20-3.22 where scrollbars
    may appear stuck (issue
    [\#3545](https://github.com/Beep6581/RawTherapee/issues/3545)), and
    where the Retinex tool's "Gain and Offset" panel may appear under
    the "Transmission" panel until the user hovers the mouse cursor over
    a curve button (issue
    [\#3525](https://github.com/Beep6581/RawTherapee/issues/3525)). For
    this reason we recommend using GTK+ 3.16-3.18 if possible.
  - RawTherapee 5 requires GCC-4.9 or higher, or Clang.
  - Do not use `-ffast-math`
  - Use `-o3`
  - For stable builds (RT5) use `-DCACHE_NAME_SUFFIX=""`
  - For development builds use `-DCACHE_NAME_SUFFIX="5-dev"`
  - Windows builders should compile on a drive letter which users are
    most unlikely to have, such as Y:, due to the "There is no disk in
    the drive" error (issue
    [\#3544](https://github.com/Beep6581/RawTherapee/issues/3544#issuecomment-267606005)).


# News Relevant to Developers

  - Use C++11
  - Code must be run through astyle.
  - Commits automatically trigger a compilation using Travis CI.


Complete revision history available on
[GitHub](https://github.com/Beep6581/RawTherapee/commits/).

