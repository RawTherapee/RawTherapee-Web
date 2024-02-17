---
title: "RawTherapee v5.9"
date: 2022-11-27T22:00:00+01:00
draft: false
version: "5.9"
linux_appimage: "https://rawtherapee.com/shared/builds/linux/RawTherapee_5.9.AppImage"
linux_binary_32: ""
linux_binary_64: ""
windows_binary: "https://rawtherapee.com/shared/builds/windows/RawTherapee_5.9_win64.zip"
windows_xp_binary: ""
mac_binary: "https://rawtherapee.com/shared/builds/mac/RawTherapee_macOS_11.7_Universal_5.9.zip"
source_code: "https://rawtherapee.com/shared/source/rawtherapee-5.9.tar.xz"
---

## Screenshot

{{< figure src="rt59_provence_local_mask.jpg" link="rt59_provence_local_mask.jpg">}}



## Windows Installation Instructions

Just open the zip file and run the executable installer.



## Linux Installation Instructions

Software should be installed through your distribution's package manager.

If RawTherapee&nbsp;5.9 is not yet available in your package manager, you can use the AppImage:

1. Download it.
1. Make it executable:
`chmod u+x RawTherapee_5.9.AppImage`
1. Run it:
`./RawTherapee_5.9.AppImage`



## macOS Installation Instructions

The macOS build requires macOS Big Sur (version 11) or newer.

To install the RawTherapee application, open the `.dmg` file and drag the RawTherapee app onto the `/Applications` folder.

To use the optional `rawtherapee-cli` command line interface, move `rawtherapee-cli` into a folder in your `$PATH` and install the RawTherapee app as above.

If the workspace is too small to read, you must change the HiDPI settings in RawTherapee: go to Preferences &gt; General, and enable "[Pseudo-HiDPI mode](https://rawpedia.rawtherapee.com/Preferences#Appearance)". Restart RawTherapee for the changes to take effect.

There is [a known issue](https://gitlab.gnome.org/GNOME/gtk/-/issues/5305) concerning macOS Ventura (version 13) wherein it may be impossible to click on some GUI elements, specifically drop-down menus. The source of this problem lies in macOS/GTK+ and is unrelated to RawTherapee. We will update you once a fix is available.



## New Features

- The Spot Removal tool (Detail tab) was added, for removing dust specks and small objects.
- The Color Appearance & Lighting tool (Advanced tab), formerly known as CIECAM02, now includes CAM16. By taking into account the conditions of the photographed scene and the conditions under which the image is viewed, it allows you to adjust the image in a way which matches human color perception.
- The Local Adjustments tool (Local tab) was added, for performing a wide range of operations on an area of the image determined by its geometry or color.
- The Wavelet Levels tool (Advanced tab) received various improvements.
- The White Balance tool (Color tab) received a new automatic white balance method named "temperature correlation" (the old one was renamed to "RGB grey").
- The Film Negative tool (Color tab) received various improvements including support for non-raw files.
- The Preprocess White Balance tool (Raw tab) was added, allowing you to specify whether channels should be balanced automatically or whether the white balance values recorded by the camera should be used instead.
- A new Perspective Correction tool (Transform tab) was added which includes an automated perspective correction feature.
- The Main Histogram was improved with new modes: waveform, vectorscope and RGB parade.
- Improvements to the Inspect feature (File Browser tab).
- New dual-demosaicing methods in the Demosaicing tool (Raw tab).
- The Haze Removal tool (Detail tab) received a saturation adjuster.
- The RawTherapee theme was improved, including changes to make it easier to see which tools are enabled.
- The Navigator (Editor tab) can now be resized.
- The Resize tool (Transform tab) now allows to resize by the long or short edge.
- The Crop tool (Transform tab) received a "centered square" crop guide, useful when the resulting non-square image will also be used on social media which crop to a square format.
- The Pixel Shift demosaicing method (Raw tab) now allows using an average of all frames for regions with motion.
- Added or improved support for cameras, raw formats and color profiles:
    - Canon EOS 100D / Rebel SL1 / Kiss X7
    - Canon EOS 1DX Mark III
    - Canon EOS 2000D / Rebel T7 / Kiss X90
    - Canon EOS 400D DIGITAL
    - Canon EOS 5D Mark II
    - Canon EOS 5D Mark IV (DCP)
    - Canon EOS 90D (DCP)
    - Canon EOS M6 Mark II (DCP)
    - Canon EOS R (DCP)
    - Canon EOS R3, R7 and R10
    - Canon EOS R5 (DCP)
    - Canon EOS R6 (DCP)
    - Canon EOS RP
    - Canon EOS-1D Mark III
    - Canon EOS-1Ds
    - Canon EOS-1Ds Mark II
    - Canon PowerShot G1 X Mark II (DCP)
    - Canon PowerShot G9 X Mark II
    - Canon PowerShot S120 (DCP)
    - Canon PowerShot SX50 HS
    - Canon PowerShot SX70 HS
    - DJI FC3170
    - FUJIFILM X-A5 (DCP)
    - FUJIFILM X-E4
    - FUJIFILM X-H1 (DCP)
    - FUJIFILM X-PRO2
    - FUJIFILM X-PRO3 (DCP)
    - FUJIFILM X-S10
    - FUJIFILM X-T1
    - FUJIFILM X-T100
    - FUJIFILM X-T2
    - FUJIFILM X-T3 (DCP)
    - FUJIFILM X-T30
    - FUJIFILM X-T4
    - FUJIFILM X100V
    - Fujifilm GFX 100
    - Fujifilm GFX100S though lossy compression and alternative crop modes (e.g. 4:3) are not supported yet
    - Fujifilm X-A20
    - Fujifilm X-T4
    - HASSELBLAD NEX-7 (Lunar)
    - Hasselblad L1D-20c (DJI Mavic 2 Pro)
    - Improved support for the Canon CR3 raw format, added support for compressed files, affects Canon EOS M50, R, R5, R6 and 1D X Mark III, etc.
    - LEICA C-LUX
    - LEICA CAM-DC25
    - LEICA D-LUX 7
    - LEICA M8
    - LEICA V-LUX 5
    - Leica SL2-S
    - NIKON COOLPIX P1000
    - NIKON D500 (DCP)
    - NIKON D5300 (DCP)
    - NIKON D610 (DCP)
    - NIKON D7100 (DCP)
    - NIKON D7500 (DCP)
    - NIKON D800 (DCP)
    - NIKON D850 (DCP)
    - NIKON Z 6 (DCP)
    - NIKON Z 7 (DCP)
    - Nikon 1 J4
    - Nikon COOLPIX P950
    - Nikon D2Hs
    - Nikon D2Xs
    - Nikon D300s
    - Nikon D3500
    - Nikon D5100
    - Nikon D6
    - Nikon D70s
    - Nikon D780
    - Nikon D810A
    - Nikon Z 5
    - Nikon Z 50 (DCP)
    - Nikon Z 6II
    - Nikon Z 7II
    - Nikon Z fc
    - OLYMPUS E-M10 Mark IV
    - OLYMPUS E-M1 Mark III
    - OLYMPUS E-M1X
    - OLYMPUS E-M5 Mark II (DCP)
    - OLYMPUS E-M5 Mark III
    - OLYMPUS E-PL10
    - OLYMPUS E-PL9
    - OLYMPUS Stylus 1
    - OLYMPUS Stylus 1s
    - OLYMPUS TG-6
    - PENTAX K-50 (DCP)
    - PENTAX K10D
    - Panasonic DC-FZ1000M2
    - Panasonic DC-FZ80
    - Panasonic DC-FZ81
    - Panasonic DC-FZ82
    - Panasonic DC-FZ83
    - Panasonic DC-G100
    - Panasonic DC-G110
    - Panasonic DC-G90
    - Panasonic DC-G95
    - Panasonic DC-G99
    - Panasonic DC-S1H
    - Panasonic DC-S5 (DCP)
    - Panasonic DC-TZ95
    - Panasonic DC-ZS80
    - Panasonic DMC-TZ80
    - Panasonic DMC-TZ85
    - Panasonic DMC-ZS60
    - RICOH PENTAX K-1 Mark II
    - RICOH PENTAX K-3 Mark III
    - SONY ILCE-9 (DCP)
    - SONY NEX-7
    - Samsung Galaxy S7
    - Sigma fp
    - Sony DCZV1B
    - Sony DSC-HX95
    - Sony DSC-HX99
    - Sony DSC-RX0
    - Sony DSC-RX0M2
    - Sony DSC-RX100
    - Sony DSC-RX100M5A
    - Sony DSC-RX100M6
    - Sony DSC-RX100M7
    - Sony DSC-RX10M2
    - Sony DSC-RX10M3
    - Sony DSC-RX10M4
    - Sony DSC-RX1R
    - Sony ILCE-1
    - Sony ILCE-6100
    - Sony ILCE-6400 (DCP)
    - Sony ILCE-6600 (DCP)
    - Sony ILCE-7C
    - Sony ILCE-7M3
    - Sony ILCE-7M4
    - Sony ILCE-7RM4 (DCP)
    - Sony ILCE-7SM3
    - Sony ILCE-9M2
    - Sony NEX-F3
    - Sony SLT-A99V



## More Information

A few months ago [Pat David](https://patdavid.net/about/) wrote the article [RawTherapee 5.9 (WIP) and Project Updates]({{< relref "2022-07-08-rawtherapee-not-dead" >}} "RawTherapee 5.9 WIP and Project Updates") which explained all the major new features and changes in RawTherapee since the release of version 5.8 in 2020. The work since then focused only on stabilization and polish to bring you this release. Read that article for more information.



## SHA-256

- `463f838981a1f11dff37160b1dc5c67a13d27066b869d8dea301db416871eb67  RawTherapee_5.9.AppImage`
- `dcc02ad33588a509da73e4a093508d795bda42dc5ece66cb6a564979bb204cc5  RawTherapee_5.9_win64.zip`



## News Relevant to Package Maintainers

New since 5.8:
- Automated build system moved from Travis CI to [GitHub Actions](https://github.com/Beep6581/RawTherapee/actions)
- libcanberra made optional in CMake via `USE_LIBCANBERRA`, default `ON`.

In general:
- To get the source code, either clone from git or use the tarball from https://rawtherapee.com/shared/source/ . Do not use the auto-generated GitHub release tarballs.
- Requires GTK+ version >=3.16, though >=3.22.24 is recommended.
- GTK+ versions 3.24.2 - 3.24.6 have an issue where combobox menu scroll-arrows are missing when the combobox list does not fit vertically on the screen. As a result, users would not be able to scroll in the following comboboxes: Processing Profiles, Film Simulation, and the camera and lens profiles in Profiled Lens Correction.
- RawTherapee 5 requires GCC-4.9 or higher, or Clang.
- Do not use `-ffast-math`, it will not make RawTherapee faster but will introduce artifacts.
- Use `-O3`, it will make RawTherapee faster with no known side-effects.
- For stable releases use `-DCACHE_NAME_SUFFIX=""`
- For development builds and release-candidates use `-DCACHE_NAME_SUFFIX="5-dev"`



## News Relevant to Developers

See [CONTRIBUTING.md](https://github.com/Beep6581/RawTherapee/blob/dev/CONTRIBUTING.md).

Complete revision history [available on GitHub](https://github.com/Beep6581/RawTherapee/commits/5.9).



## Reporting Bugs

If you found a problem, don't keep it to yourself. Read the article "[How to Write Useful Bug Reports](https://rawpedia.rawtherapee.com/How_to_write_useful_bug_reports)" to get the problem fixed.
