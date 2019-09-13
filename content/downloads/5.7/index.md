---
title: "RawTherapee v5.7"
date: 2019-09-10T15:39:50+02:00
draft: false
version: "5.7"
linux_appimage: "https://rawtherapee.com/shared/builds/linux/RawTherapee-releases-5.7-20190910.AppImage"
linux_binary_32: ""
linux_binary_64: ""
windows_binary: "https://rawtherapee.com/shared/builds/windows/RawTherapee_5.7_WinVista_64.zip"
windows_xp_binary: ""
mac_binary: ""
source_code: "https://rawtherapee.com/shared/source/rawtherapee-5.7.tar.xz"
---

RawTherapee 5.7 has been released\!

{{< figure src="rt57_drosera_rotundifolia.jpg" >}}

## New Features

- Film Negative tool, for easily developing raw photographs of film negatives.
- Support for reading "rating" tags from Exif and XMP, shown in the File Browser/Filmstrip using RawTherapee's star rating system.
- Hundreds of bug fixes, speed optimizations and raw format support improvements.

RawTherapee and other open-source projects require access to sample raw files from various camera makes and models in order to support those raw formats correctly. You can help by submitting raw files to RPU: https://raw.pixls.us/

## News Relevant to Package Maintainers

New since 5.6:

- Requires CMake >=3.5.

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

Complete revision history [available on GitHub](https://github.com/Beep6581/RawTherapee/commits/5.7).
