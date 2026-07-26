---
title: "RawTherapee v5.13"
date: 2026-07-26T00:07:00+00:00
draft: false
version: "5.13"
linux_appimage: "https://rawtherapee.com/shared/builds/linux/RawTherapee_5.13_release.AppImage"
linux_arm_appimage: "https://rawtherapee.com/shared/builds/linux/RawTherapee_5.13_arm_release.AppImage"
linux_binary_32: ""
linux_binary_64: ""
windows_binary: "https://rawtherapee.com/shared/builds/windows/RawTherapee_5.13_win64_release.exe"
windows_arm_binary: "https://rawtherapee.com/shared/builds/windows/RawTherapee_5.13_win64_arm_release.exe"
windows_xp_binary: ""
mac_binary: "https://rawtherapee.com/shared/builds/mac/RawTherapee_MacOS_26.0_Universal_5.13.zip"
source_code: "https://rawtherapee.com/shared/source/rawtherapee-5.13.tar.xz"
---

{{< figure src="splash.svg" >}}

## New Features

- The Gamut Compression tool received several enhancements:
    - The maximum values for the distance limits has been increased.
    - The distance limits can be set automatically.
    - The tool now shows the maximum red, green, blue, and achromatic values, as well as the estimated distance ratio between the working and target color spaces.
- The Abstract Profile tool in Color Management received several enhancements:
    - Highlight attenuation can be adjusted rather than simply being on or off.
    - There is a new custom destination primaries option that allows changing the primaries by hue and saturation.
    - The xy chromaticity diagram in the primaries adjustment shows the Rec2020 primaries for reference.
- The Color Appearance & Lighting tool received several enhancements.
- The Selective Editing's Equalization & Pre-Tone Mapping (formerly Shadows/Highlights, Equalizer & GHS) tool has a new simple tone mapper called Michaelis-Menten.
- The Generalized Hyperbolic Stretch (GHS) method in Selective Editing's Equalization & Pre-Tone Mapping (formerly Shadows/Highlights, Equalizer & GHS) tool received several enhancements:
    - The Black point and White point can be set automatically.
    - The Black point/White point section now shows the maximum red, green, and blue values and the dynamic range.
    - There is now a choice of matrix conversions that affect the color handling.
    - Several parameters can now be adjusted regardless of what the Stretch Factor (D) is set to.
    - The Symmetry point shows a recommended value and can be set automatically.
    - Middle gray, RGB maximum, and 3 sigma standard deviation are displayed.
- In Selective Editing's Color Appearance tool, the Source Data Adjustments section has a new TRC based tone mapper with per-channel TRC adjustment and a color inversion option. The RGB channel slope tone mapper also received the color inversion option.
- The Blur/Grain & Denoise tool in Selective Editing received several enhancements:
    - A new Recovery Based on Luminance Mask in Blur & Noise allows refining the blurred area.
    - Denoise has new options to reduce denoising of details.
- Selective Editing's Sharpening tool has a new Capture Deconvolution method which brings the benefits of Capture Sharpening to Selective Editing and works on both raw and non-raw images.
- The Crop tool guides has been revamped to allow multiple guides to be shown simultaneously, the guides' color to be changed, alternative aspect ratios to be shown, and a bleed area to be set.
- The Lens / Geometry tool can scale images horizontally or vertically.
- The Capture Sharpening tool has a new Presharpening denoise option which can improve the sharpening result on noisy images by creating a better contrast mask.
- The File Browser can show color labels from XMPs embedded in image files.
- In the Queue's Output Location template, a new "%e" format specifier is
available which expands to the file extension of the output file (for example, "jpg" or "png").
- HiDPI support is improved, most notably making the editor preview and thumbnails sharp.
- All profiles are now shown in the monitor profile selection in Preferences.
- Performance on ARM has been improved.
- All preferences can now be easily reset in Preferences.
- Adapted Olympus lens name detection is improved.
- Added new translations for Hebrew and Korean.
- Updated translations for Simplified Chinese, Dutch, and German.
- Added or improved support for cameras, raw formats, and color profiles (not an exhaustive list because unconfirmed support is excluded):
    - Canon EOS M50 (white level)
    - Canon EOS R5m2
    - Canon EOS R6 Mark III (black level)
    - Canon EOS R50 V (black level)
    - Canon EOS R100 (white level)
    - Canon PowerShot V1 (black level, white level)
    - Fujifilm GFX 50S II (color matrix)
    - Fujifilm GFX 50S II (color matrix)
    - Fujifilm GFX 100 II (color matrix)
    - Fujifilm X-M5 (color matrix, raw crop)
    - Fujifilm X-T30 III (raw crop)
    - Hasselblad CFV-100c (color matrix)
    - Nikon Z5_2 (color matrix)
    - Nikon Z50_2 (color matrix)
    - Nikon Z f (white level)
    - Olympus OM-3 (color matrix)
    - Olympus OM-5MarkII (color matrix)
    - Panasonic DC-G97 (color matrix)
    - Panasonic DC-S1M2ES (raw crop)
    - Panasonic DC-S1M2 (raw crop)
    - Panasonic DC-S1RM2 (raw crop)
    - Panasonic DC-S9 (raw crop)
    - Samsung DNGs (black level, white level)
    - Sony DSC-RX1RM3 (raw crop)
    - Sony ILCE-1M2 (color matrix, raw crop)
    - Sony ILCE-7M5 (black level, raw crop)
    - Sony ILCE-6400A (color matrix)



## Other Important Changes Since 5.12
- The default working profile is now Rec2020 instead of ProPhoto.
    - **Why it changed:** ProPhoto has a very large gamut. While it is useful for preventing loss of color information during editing, it also allows colors that cannot exist in the real world. Some tools work best when there are only real colors. Rec2020 also has a large gamut, but only allows real colors.
    - **What it means for you:** ProPhoto is still available. Use of Rec2020 is completely optional. If you previously used ProPhoto and decide to switch to Rec2020, be aware that some tools are dependent on the working profile and may behave differently. Examples include, but are not limited to, Exposure, Channel Mixer, HSV Equalizer, Soft Light, RGB Curves, and Color Toning.



## LibRaw

LibRaw is a software component used to read raw files. RawTherapee had always used a different raw file reader: an enhanced version of dcraw. dcraw has not been updated in 8 years, making it a burden on RawTherapee developers to support new cameras. Starting in 5.11, RawTherapee can use LibRaw to read raw files. If LibRaw determines it cannot read a raw file, RawTherapee will fall back to the enhanced dcraw. Official packages distributed by the RawTherapee team contain an enhanced LibRaw. Unofficial packages distributed by 3rd parties may decide to use a different version of LibRaw, which may not support as many cameras.

Switching to LibRaw is a significant change. Although LibRaw originated from dcraw and the RawTherapee team made an effort to ensure the smoothest transition, there may be some raw files that LibRaw cannot handle as adequately as the enhanced dcraw. If you encounter this scenario, please submit a bug report as described below in [Reporting Bugs](#reporting-bugs). LibRaw can be disabled in the preferences. Keep in mind the enhanced dcraw cannot read certain raw images that LibRaw can. LibRaw will become mandatory in a future version of RawTherapee, so don't keep those bugs to yourself!



## Installation Instructions

Find the installation instructions for your operating system below.

Please note that there are two downloads available for Windows and Linux. One is for x86_64 CPUs, such as those from Intel and AMD, while the other one is for ARM64 CPUs, such as those from Qualcomm. Make sure to download the correct one for your CPU. If you are not sure which type of CPU your computer has, try running both versions and see which one works.



### Windows

Just open the zip file and run the executable installer.



### Linux

Software should be installed through your distribution's package manager.

If RawTherapee&nbsp;5.13 is not yet available in your package manager, you can use the AppImage:

For x86_64 CPUs:

1. Download it.
1. Make it executable:
`chmod u+x RawTherapee_5.13_release.AppImage`
1. Run it:
`./RawTherapee_5.13_release.AppImage`

For ARM CPUs:

1. Download it.
1. Make it executable:
`chmod u+x RawTherapee_5.13_arm_release.AppImage`
1. Run it:
`./RawTherapee_5.13_arm_release.AppImage`



### macOS

The macOS build requires macOS Tahoe 26.0 or newer on Apple Silicon or macOS Monterey 12.0 or newer for Intel (x86_64).

To install the RawTherapee application, unzip the `.zip` file, open the `.dmg` file, and drag the RawTherapee app onto the `/Applications` folder. For security reasons, RawTherapee MUST be installed in `/Applications`. RawTherapee will refuse to start if installed elsewhere. Do not move or rename RawTherapee.app.

To use the optional `rawtherapee-cli` command line interface, move `rawtherapee-cli` into a folder in your `$PATH` and install the RawTherapee app as above.



## SHA-256

- `746a3509a234804c3a5f66649006ac29ac67f193a8559d2297357949a890b097 RawTherapee_5.13_release.AppImage`
- `9e424633272a49bb47afe4bf065604858acf9de77c4d80e0f6557024492e2b55 RawTherapee_5.13_arm_release.AppImage`
- `d27df7ebde717c5efa114338a4b1cf1c426a439e5a1a92e142e87868cbe45383 RawTherapee_5.13_win64_release.exe`
- `967fc854266a1ab3629e2c23ddbfcd193cb71d996ffe16fe2a542d3610701cd2 RawTherapee_5.13_win64_arm_release.exe`
- `795a32a688afa5b127dfd768c25c77649859ababa206352e865f6587c66c45a7 RawTherapee_MacOS_26.0_Universal_5.13.zip`
- `23bdff4b1817e1274c11a94b11d21cac59e9c1b1d209795d3194710ee73e77bf rawtherapee-5.13.tar.xz`



## Reporting Bugs

If you found a problem, don't keep it to yourself. Read the article "[How to Write Useful Bug Reports](https://rawpedia.rawtherapee.com/How_to_write_useful_bug_reports)" to get the problem fixed.



## News Relevant to Package Maintainers

New since 5.12:
- RawTherapee may be built to use LunaSVG instead of librsvg.
- RawTherapee may be compiled with SIMDe to improve performance on ARM architectures.
- The `USE_OLD_CXX_ABI` option has been removed.
- RawTherapee depends on the fmt library. By default, it will download the source code and build it. To use the system fmt library, use `-DWITH_SYSTEM_FMT="ON"`.

In general:
- To get the source code, either clone from git or use the tarball from https://rawtherapee.com/shared/source/. Do not use the auto-generated GitHub release tarballs.
- Requires GTK+ version >= 3.24.3.
- GTK+ versions 3.24.3 - 3.24.6 have an issue where combobox menu scroll-arrows are missing when the combobox list does not fit vertically on the screen. As a result, users would not be able to scroll in the following comboboxes: Processing Profiles, Film Simulation, and the camera and lens profiles in Profiled Lens Correction.
- JPEG XL read support depends on libjxl. By default, RawTherapee builds with JPEG XL support if and only if libjxl is present. Use `-DWITH_JXL="ON"` or `-DWITH_JXL="OFF"` to explicitly enable or disable, respectively, JPEG XL support.
- RawTherapee builds with a custom version of LibRaw by default. To use the system LibRaw, use `-DWITH_SYSTEM_LIBRAW="ON"`. Requires LibRaw >= 0.21.
- To avoid Rust dependencies, build using the LunaSVG rendering backend with `-DSVG_BACKEND="lunasvg"`. Use `-DWITH_SYSTEM_LUNASVG="ON"` to use the system LunaSVG.
- RawTherapee has hand-optimized code for most x86_64 architectures. SIMDe is an optional compile-time dependency that allows most of the optimizations to be used on arm64. Enable it with `-DWITH_SIMDE="ON"`.
- RawTherapee 5 requires GCC-4.9 or higher, or Clang.
- Do not use `-ffast-math`, it will not make RawTherapee faster but will introduce artifacts.
- Use `-O3`, it will make RawTherapee faster with no known side-effects.
- For stable releases use `-DCACHE_NAME_SUFFIX=""`
- For development builds and release-candidates use `-DCACHE_NAME_SUFFIX="5-dev"`



## News Relevant to Developers

See [CONTRIBUTING.md](https://github.com/RawTherapee/RawTherapee/blob/dev/CONTRIBUTING.md).

Complete revision history [available on GitHub](https://github.com/RawTherapee/RawTherapee/commits/5.13).
