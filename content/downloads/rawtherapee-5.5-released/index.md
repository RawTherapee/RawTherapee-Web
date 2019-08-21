---
title: "RawTherapee 5.5 Released"
date: 2018-12-17T17:01:00+00:00
author: DrSlony
draft: false
version: ""
linux_binary: "https://rawtherapee.com/releases_head/linux/RawTherapee-releases-5.5-20181217.AppImage"
windows_binary: "https://rawtherapee.com/releases_head/windows/RawTherapee_5.5_WinVista_64.zip"
mac_binary: "https://rawtherapee.com/releases_head/mac/RawTherapee_OSX_10.9_64_5.5.zip"
source_code: ""
---



RawTherapee 5.5 has been released\!


{{< figure src="rt_splash_5.5.png" >}}


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

  - A Windows installer is available from our [Downloads](/downloads)
    page.
  - A macOS disk image is available from our [Downloads](/downloads)
    page.
  - Linux users can get RawTherapee from their package managers, or get
    the AppImage from our [Downloads](/downloads) page.
  - Compiling yourself? Grab a no-git-required
    [tarball](http://rawtherapee.com/shared/source/) or `git
    checkout 5.5`, then read the
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

## New Features since 5.4:

  - Filter to remove [striping
    artifacts](http://rawpedia.rawtherapee.com/Preprocessing#PDAF_Lines_Filter)
    caused by Phase Detection Auto Focus (PDAF) as seen in Sony cameras,
    and to remove [banding
    artifacts](http://rawpedia.rawtherapee.com/Preprocessing#Nikon_PDAF_Banding)
    caused by Nikon's too-aggressive in-camera PDAF correction. These
    are available for any camera which has a PDAF entry in
    camconst.json, currently:
      - Nikon Z 6
      - Nikon Z 7
      - Sony DSC-RX1RM2
      - Sony ILCE-6000
      - Sony ILCE-6300
      - Sony ILCE-6500
      - Sony ILCE-7M3
      - Sony ILCE-7RM2
      - Sony ILCE-7RM3
      - Sony ILCE-9
    {{< figure src="rt55_pdaf_lines_filter_sony.png" link="rt55_pdaf_lines_filter_sony.png" >}}
    {{< figure src="rt55_pdaf_banding_nikon.png" link="rt55_pdaf_banding_nikon.png" >}}
  - [Out-of-gamut
    warning](http://rawpedia.rawtherapee.com/The_Image_Editor_Tab#Monitor_Profile_and_Soft-Proofing)
    compatible with ICC v2 and v4 profiles.
    {{< figure src="rt55_out_of_gamut.png" link="rt55_out_of_gamut.png" >}}
  - Ability to specify [custom working color
    spaces](http://rawpedia.rawtherapee.com/Color_Management#Adding_Custom_Working_Profiles)
    through the `workingspaces.json` file.
  - Unbounded processing - allows you to decide whether out-of-gamut
    colors should get clipped.
  - Improved support for Canon mRaw format variants.
  - New
    [Shadows/Highlights](http://rawpedia.rawtherapee.com/Shadows/Highlights)
    tool (replaced previous one).
  - Contrast threshold mask which divides an image into areas of high
    and low detail, allowing the effect of certain tools to be focused
    where it matters most and to mitigate the effect on areas where it
    would be undesirable, for example having the Sharpening tool affect
    only the in-focus subject without affecting the out-of-focus
    background. Available for:
      - Sharpening
      - Post-Resize Sharpening
      - Microcontrast
      - Demosaicing
    {{< figure src="rt55_contrast_threshold_sharpening.png" link="rt55_contrast_threshold_sharpening.png" >}}
  - Dual-demosaic algorithms, making use of the new contrast threshold
    mask, allowing one to use a combination of demosaicing algorithms
    where one is best for details and the other best for plain areas.
  - New [color toning](http://rawpedia.rawtherapee.com/Color_Toning)
    methods:
      - [Grid](http://rawpedia.rawtherapee.com/Color_Toning#L.2Aa.2Ab.2A_Color_Correction_Grid),
        allowing you to separately tone the shadows and highlights using
        two points on a simple color grid.
      - [Regions](http://rawpedia.rawtherapee.com/Color_Toning#Color_Correction_Regions),
        allowing you to tone based on any number of masks. Supports
        functions from the American Society of Cinematographers Color
        Decision List (ASC CDL).
    {{< figure src="rt55_color_toning_grids_1_mask_on.png" link="rt55_color_toning_grids_1_mask_on.png" >}}
    {{< figure src="rt55_color_toning_grids_1_mask_off.png" link="rt55_color_toning_grids_1_mask_off.png" >}}
  - Resizable [main
    histogram](http://rawpedia.rawtherapee.com/The_Image_Editor_Tab#Main_Histogram)
    with scaling modes:
      - Linear
      - Log
      - Log-Log
    The log scales can be adjusted by click-dragging the mouse sideways
    inside the histogram area.
    {{< figure src="rt54_vs_55_histograms.png" link="rt54_vs_55_histograms.png" >}}
  - Support for Blackmagic and Canon Magic Lantern lj92 encoded files.
  - Allows you to specify how many border rows/columns to discard during
    demosaicing - those who shoot raw video at a standard resolution
    such as 1920x1080 will appreciate being able to preserve the
    dimensions.
  - New [Soft Light](http://rawpedia.rawtherapee.com/Soft_Light) tool
    which enhances contrast and saturation by emulating the effect of
    blending an image with a copy of itself in "soft light" blending
    mode in GIMP.
    {{< figure src="rt55_soft_light.png" link="rt55_soft_light.png" >}}
  - New [Haze Removal](http://rawpedia.rawtherapee.com/Haze_Removal)
    tool to reduce the effects of haze or fog.
    {{< figure src="rt55_haze_removal_1.png" link="rt55_haze_removal_1.png" >}}
    {{< figure src="rt55_haze_removal_2.png" link="rt55_haze_removal_2.png" >}}
  - The [Resize](http://rawpedia.rawtherapee.com/Resize) tool allows you
    to specify whether you want it to upscale or only downscale.
  - New icon and cursor theme.
  - [ICC profile creator](http://rawpedia.rawtherapee.com/ICC_Profile_Creator).
    {{< figure src="rt55_icc_profile_creator.png" link="rt55_icc_profile_creator.png" >}}
  - The bundled ICC profiles have been re-generated, and now include ICC
    v2 and v4 variants.
  - If your screen's resolution is such that not all icons fit in a
    toolbar, you can now scroll the toolbar using the mouse
    scroll-wheel.
  - New "[Flexible](http://rawpedia.rawtherapee.com/Exposure#Flexible)"
    tone curve type. A characteristic of the cubic spline curve (renamed
    from "Custom" to
    "[Standard](http://rawpedia.rawtherapee.com/Exposure#Standard)") is
    that editing one node could have a huge impact on what happens to
    the curve in relation to the other nodes. The new "Flexible"
    centripetal Catmull–Rom spline curve allows you to make adjustments
    to any part of the curve with little impact on the other parts.
    {{< figure src="rt54_vs_55_curves.png" link="rt54_vs_55_curves.png" >}}
  - Allow saving both floating-point and integer type files at both
    16-bit and 32-bit precision from RawTherapee GUI and CLI.
  - Improved lensfun chromatic aberration correction.
  - The raw chromatic aberration correction tool can now run in several
    iterations, and gained a feature to avoid introducing a color shift
    which could result from correcting chromatic aberration before
    demosaicing.
  - Certain sliders now operate on a logarithmic scale, allowing for a
    meaningful response over large ranges.
  - Dedicated "Reset" button in Crop tool.
  - Support for new cameras, and new input color profiles.
  - Speed enhancements and bug fixes, for a total of over 1300 commits.

RawTherapee and other open-source projects require access to sample raw
files from various camera makes and models in order to support those raw
formats correctly. You can help by submitting raw files to RPU:
<https://raw.pixls.us/>


# News Relevant to Package Maintainers

Changes since 5.4:

  - Requires libtiff \>= 4.0.4.
  - Requires CMake \>= 2.8.8.
  - Optional codesigning commands have been added to the CMakeLists.txt
    and macosx\_bundle.sh scripts. If you wish to codesign the built
    packages (.app and .dmg), add your details to your CMake command
    flags:
    `-DCODESIGNID:STRING="Developer ID Application: Firstname Lastname
    (xxx)"`

In general:

  - To get the source code, either clone from git or use the tarball
    from <http://rawtherapee.com/shared/source/> . Do not use the
    auto-generated GitHub release tarballs.
  - Requires GTK+ version \>=3.16, though \>=3.22.24 is recommended.
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
[GitHub](https://github.com/Beep6581/RawTherapee/commits/5.5).
