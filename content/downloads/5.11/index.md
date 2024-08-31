---
title: "RawTherapee v5.11"
date: 2024-08-25T00:00:00+00:00
draft: false
version: "5.11"
linux_appimage: "https://rawtherapee.com/shared/builds/linux/RawTherapee_5.11_release.AppImage"
linux_binary_32: ""
linux_binary_64: ""
windows_binary: "https://rawtherapee.com/shared/builds/windows/RawTherapee_5.11_win64_release.exe"
windows_xp_binary: ""
mac_binary: "https://rawtherapee.com/shared/builds/mac/RawTherapee_macOS_12.3_Universal_5.11.zip"
source_code: "https://rawtherapee.com/shared/source/rawtherapee-5.11.tar.xz"
---

## Screenshot

{{< figure src="vast-beach.jpg" link="vast-beach.jpg">}}



## Windows Installation Instructions

Just run the executable installer and follow the prompts.



## Linux Installation Instructions

Software should be installed through your distribution's package manager.

If RawTherapee 5.11 is not yet available in your package manager, you can use the AppImage:

1. Download it.
1. Make it executable:
`chmod u+x RawTherapee_5.11.AppImage`
1. Run it:
`./RawTherapee_5.11.AppImage`



## macOS Installation Instructions

The macOS build requires macOS Monterey 12.3 or newer.

To install the RawTherapee application, unzip the `.zip` file, open the `.dmg` file, and drag the RawTherapee app onto the `/Applications` folder. For security reasons, RawTherapee MUST be installed in `/Applications`. RawTherapee will refuse to start if installed elsewhere. Do not move or rename RawTherapee.app.

To use the optional `rawtherapee-cli` command line interface, move `rawtherapee-cli` into a folder in your `$PATH` and install the RawTherapee app as above.



## New Features

- The path template for queue export supports more format specifiers, including dates and new path types. Additionally, there is a preview to show the path for the selected image.
- The maximum zoom for the editor is now configurable.
- Pseudo HiDPI is replaced by real HiDPI.
- The file browser has an option to show all images within subfolders too.
- The Use embedded option for the Input Profile is available for DNGs that have an embedded DCP.
- The Color appearance sub-tool in Selective Editing (formerly Local Adjustments) received various improvements, including simplification of the basic mode, addition of new tone mappers for Cam16, a black and white mode, and a highlight attenuation feature.
- The White balance Tint range is expanded.
- It is now possible to use Contrast by Detail Levels in Before Black-and-White mode while Color Appearance & Lighting is activated with CAM16.
- Ratings and color labels can be synchronized with XMPs.
- The Selective Editing tool received various improvements, such as a global mode for applying edits to the entire image uniformly, ΔE preview buttons for most sub-tools, and adjustable graduated filter feathering for each sub-tool.
- The EXIF modified date-time is now added to saved images.
- RawTherapee can now read 12-bit Panasonic raw files encoded in the v6 format, such as those from the DC-GH5M2.
- RawTherapee can now read Panasonic raw files encoded in the v8 format, such as those from the DC-GH6, DC-S5M2, and DC-S5M2X.
- RawTherapee can now read Fujifilm lossy-compressed raw files.
- JPEG XL images can now be opened.
- There is a new option to use lens corrections from the file metadata. It works for compatible raw images from Fujifilm, Olympus / OM Digital Solutions (distortion and chromatic aberration corrections only), and Sony. Corrections embedded in DNGs can also be used.
- RawTherapee can leverage LibRaw (enabled by default) to read raw images. It adds the ability to read additional raw formats, such as Sony lossless compression, and improved support for some cameras.
- Added or improved support for cameras, raw formats and color profiles (not including LibRaw and color matrices for dcraw):
    - FUJIFILM GFX 100 (PDAF lines filter)
    - FUJIFILM GFX 100S (DCP, PDAF lines filter)
    - FUJIFILM GFX 100 II (PDAF lines filter)
    - Fujifilm X-H2S
    - Nikon Z 8 (DCP)
    - Nikon Z 9 (DCP)
    - Nikon Z f (DCP)
    - OM Digital Solutions TG-7
    - Panasonic DC-G9M2
    - Panasonic DC-GH5M2
    - Panasonic DC-GH6
    - Panasonic DC-S5M2
    - Panasonic DC-S5M2X
    - Sony ILCE-1 (Pixel shift)
    - Sony ILCE-6700
    - Sony ILCE-7CR (PDAF lines filter)
    - Sony ILCE-7RM4 (PDAF lines filter)
    - Sony ILCE-7RM5 (PDAF lines filter)
    - SONY ILCE-9M3



## Local Adjustments

Local Adjustments is now known as "Selective Editing".



## LibRaw

LibRaw is a software component used to read raw files. RawTherapee had always used a different raw file reader: an enhanced version of dcraw. dcraw has not been updated in 6 years, making it a burden on RawTherapee developers to support new cameras. Starting in 5.11, RawTherapee can use LibRaw to read raw files. If LibRaw determines it cannot read a raw file, RawTherapee will fall back to the enhanced dcraw. Official packages distributed by the RawTherapee team contain an enhanced LibRaw. Unofficial packages distributed by 3rd parties may decide to use a different version of LibRaw, which may not support as many cameras.

Switching to LibRaw is a significant change. Although LibRaw originated from dcraw and the RawTherapee team made an effort to ensure the smoothest transition, there may be some raw files that LibRaw cannot handle as adequately as the enhanced dcraw. If you encounter this scenario, please submit a bug report as described below in [Reporting Bugs](#reporting-bugs). LibRaw can be disabled in the preferences. Keep in mind the enhanced dcraw cannot read certain raw images that LibRaw can. LibRaw will become mandatory in a future version of RawTherapee, so don't keep those bugs to yourself!



## SHA-256

- `0acc36317f61491e935bacbbac0e34043640e2b8defec4f9933cbdf25b2f202e  RawTherapee_5.11_release.AppImage`
- `cf5515697c23f13e9b216163b45d2abf1de352276adf7f065d154e35c146c2ca  RawTherapee_5.11_win64_release.exe`
- `a3e928cafc7a00a090dcf50b84cd45af48ce8f457269d601d301072df7e0f7af  RawTherapee_macOS_12.3_Universal_5.11.zip`
- `e584c18dec112de29954b2b6471449a302a85e5cca4e42ede75fa333a36de724  rawtherapee-5.11.tar.xz`



## News Relevant to Package Maintainers

New since 5.10:
- Requires GTK+ >= 3.24.3 (was >= 3.22.24 in Windows, or >= 3.16 in other operating systems).
- Requires librsvg-2.0 >= 2.52 (was >= 2.40).
- Optional dependency on libjxl.
- Optional dependency on LibRaw >= 0.21.

In general:
- To get the source code, either clone from git or use the tarball from https://rawtherapee.com/shared/source/. Do not use the auto-generated GitHub release tarballs.
- Requires GTK+ version >= 3.24.3.
- GTK+ versions 3.24.3 - 3.24.6 have an issue where combobox menu scroll-arrows are missing when the combobox list does not fit vertically on the screen. As a result, users would not be able to scroll in the following comboboxes: Processing Profiles, Film Simulation, and the camera and lens profiles in Profiled Lens Correction.
- JPEG XL read support depends on libjxl. By default, RawTherapee builds with JPEG XL support if and only if libjxl is present. Use `-DWITH_JXL="ON"` or `-DWITH_JXL="OFF"` to explicitly enable or disable, respectively, JPEG XL support.
- RawTherapee builds with a custom version of LibRaw by default. To use the system LibRaw, use `-DWITH_SYSTEM_LIBRAW="ON"`. Requires LibRaw >= 0.21.
- RawTherapee 5 requires GCC-4.9 or higher, or Clang.
- Do not use `-ffast-math`, it will not make RawTherapee faster but will introduce artifacts.
- Use `-O3`, it will make RawTherapee faster with no known side-effects.
- For stable releases use `-DCACHE_NAME_SUFFIX=""`
- For development builds and release-candidates use `-DCACHE_NAME_SUFFIX="5-dev"`



## News Relevant to Developers

See [CONTRIBUTING.md](https://github.com/Beep6581/RawTherapee/blob/dev/CONTRIBUTING.md).

Complete revision history [available on GitHub](https://github.com/Beep6581/RawTherapee/commits/5.11).



## Reporting Bugs

If you found a problem, don't keep it to yourself. Read the article "[How to Write Useful Bug Reports](https://rawpedia.rawtherapee.com/How_to_write_useful_bug_reports)" to get the problem fixed.
