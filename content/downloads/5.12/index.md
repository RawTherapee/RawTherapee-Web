---
title: "RawTherapee v5.12"
date: 2025-05-04T00:00:00+00:00
draft: true
version: "5.12"
linux_appimage: "https://rawtherapee.com/shared/builds/linux/RawTherapee_5.12.AppImage"
linux_binary_32: ""
linux_binary_64: ""
windows_binary: "https://rawtherapee.com/shared/builds/windows/RawTherapee_5.12_win64.zip"
windows_xp_binary: ""
mac_binary: "https://rawtherapee.com/shared/builds/mac/RawTherapee_macOS_TODO_Universal_5.12.zip"
source_code: "https://rawtherapee.com/shared/source/rawtherapee-5.12.tar.xz"
---

## New Features

- The Raw Black Points has a new option called Dehaze. It sets the black points to the minimum values in the image, which often has the effect of reducing haze.
- Distortion Correction gained a de-fish feature that converts fisheye images into normal (rectilinear) images. It works best with the equidistant fisheye projection. The new Scale adjuster in Lens / Geometry allows manual scaling of the transformed image for when Auto-fill yields unsatisfactory results.
- All images in a Canon RAW burst mode file are accessible. Previously, only the first 6 images were accessible.
- A new tool called Gamut Compression applies the ACES (Academy Color Encoding System) Reference Gamut Compression operator to improve the look of highly-saturated colors and bring colors within a selectable gamut before applying other color-related tools offered by RawTherapee.
- The Resize tool gained a framing feature that adds a decorative solid color border around the image before it is saved. Various sizing options allow great flexibility in adjusting the border thickness and image dimensions. To reflect the tool's capabilities, it has been renamed to Resize & Framing.
- Demosaiced floating-point DNGs are now supported.
- The Abstract Profile tool has a new Contrast Enhancement feature that offers a simple way to add local contrast. It can be used to restore contrast lost due to the application of the abstract profile.
- The Color appearance tool in Selective Editing gained several Tone Mapping Operators (formerly Highlight Attenuation & Levels) enhancements in Source Data Adjustments. The RGB channel Slope tone mapper (formerly Levels) has new options. There is a new Sigmoid based tone mapper.
- More Sony lenses are recognized, improving the data displayed in the quick info overlay and enabling automatic profiled lens correction.
- The Shadows/Highlights & Tone Equalizer tool in Selective Editing gained the Generalized Hyperbolic Stretch (GHS) global tone mapper. To reflect the tool's new tone mapper, it has been renamed to Shadows/Highlights, Equalizer & GHS.
- Added or improved support for cameras, raw formats and color profiles (not an exhaustive list because unconfirmed support is excluded):
    - Canon EOS R8 (DCP, black level in electronic shutter mode)
    - Fujifilm X-E4 (raw crop in electronic shutter mode)
    - Sony ILCE-7CR (pixel shift)
    - Sony ILCE-7M3 (black level)
    - Sony ILME-FX3 (black level when not using LibRaw)



## LibRaw

LibRaw is a software component used to read raw files. RawTherapee had always used a different raw file reader: an enhanced version of dcraw. dcraw has not been updated in almost 7 years, making it a burden on RawTherapee developers to support new cameras. Starting in 5.11, RawTherapee can use LibRaw to read raw files. If LibRaw determines it cannot read a raw file, RawTherapee will fall back to the enhanced dcraw. Official packages distributed by the RawTherapee team contain an enhanced LibRaw. Unofficial packages distributed by 3rd parties may decide to use a different version of LibRaw, which may not support as many cameras.

Switching to LibRaw is a significant change. Although LibRaw originated from dcraw and the RawTherapee team made an effort to ensure the smoothest transition, there may be some raw files that LibRaw cannot handle as adequately as the enhanced dcraw. If you encounter this scenario, please submit a bug report as described below in [Reporting Bugs](#reporting-bugs). LibRaw can be disabled in the preferences. Keep in mind the enhanced dcraw cannot read certain raw images that LibRaw can. LibRaw will become mandatory in a future version of RawTherapee, so don't keep those bugs to yourself!



## Installation Instructions

Find the installation instructions for your operating system below.



### Windows

Just open the zip file and run the executable installer.



### Linux

Software should be installed through your distribution's package manager.

If RawTherapee&nbsp;5.12 is not yet available in your package manager, you can use the AppImage:

1. Download it.
1. Make it executable:
`chmod u+x RawTherapee_5.12.AppImage`
1. Run it:
`./RawTherapee_5.12.AppImage`



### macOS

The macOS build requires macOS TODO (version TODO) or newer.

To install the RawTherapee application, unzip the `.zip` file, open the `.dmg` file, and drag the RawTherapee app onto the `/Applications` folder. For security reasons, RawTherapee MUST be installed in `/Applications`. RawTherapee will refuse to start if installed elsewhere. Do not move or rename RawTherapee.app.

To use the optional `rawtherapee-cli` command line interface, move `rawtherapee-cli` into a folder in your `$PATH` and install the RawTherapee app as above.



## SHA-256

- `TODO  RawTherapee_5.12_release.AppImage`
- `TODO  RawTherapee_5.12_win64_release.exe`
- `TODO  RawTherapee_macOS_TODO_Universal_5.12.zip`
- `TODO  rawtherapee-5.12.tar.xz`



## Reporting Bugs

If you found a problem, don't keep it to yourself. Read the article "[How to Write Useful Bug Reports](https://rawpedia.rawtherapee.com/How_to_write_useful_bug_reports)" to get the problem fixed.



## News Relevant to Package Maintainers

New since 5.11:
- The official repository has been moved to a new GitHub organization called RawTherapee. The repository is now at https://github.com/RawTherapee/RawTherapee. Previously, it was at https://github.com/Beep6581/RawTherapee.

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

See [CONTRIBUTING.md](https://github.com/RawTherapee/RawTherapee/blob/dev/CONTRIBUTING.md).

Complete revision history [available on GitHub](https://github.com/RawTherapee/RawTherapee/commits/5.12).
