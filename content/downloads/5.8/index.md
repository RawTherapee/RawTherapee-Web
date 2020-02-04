---
title: "RawTherapee v5.8"
date: 2020-02-04T08:00:00+01:00
draft: false
version: "5.8"
linux_appimage: "https://rawtherapee.com/shared/builds/linux/RawTherapee_5.8.AppImage"
linux_binary_32: ""
linux_binary_64: ""
windows_binary: "https://rawtherapee.com/shared/builds/windows/RawTherapee_5.8_win64.zip"
windows_xp_binary: ""
mac_binary: ""
source_code: "https://rawtherapee.com/shared/source/rawtherapee-5.8.tar.xz"
---

RawTherapee 5.8 has been released\!

{{< figure src="rt58_amanita_muscaria_capture_sharpening.jpg" link="rt58_amanita_muscaria_capture_sharpening.jpg">}}

## New Features

- Automatically recover detail lost to lens blur (diffraction) using the new Capture Sharpening tool, located in the "Raw" tab. It takes place right after demosaicing, and as it works in linear space it is not prone to haloing. Capture Sharpening in combination with Post-Resize Sharpening allows for detailed and crisp results.
- CR3 support: image data is decoded so you can process your raw files, but metadata is not supported yet. If you have an ICC or DCP input profile for your CR3-producing camera, you will need to point RawTherapee to it manually (Color tab &gt; Color Management &gt; Input Profile &gt; Custom).
- Improvements of various camera models (new DCP dual-illuminant input profiles, raw crops, white levels, etc.), speedups and optimizations to various tools, better memory management, various bug fixes. See the git log for details.

RawTherapee and other open-source projects require access to sample raw files from various camera makes and models in order to support those raw formats correctly. You can help by submitting raw files to RPU: https://raw.pixls.us/

## News Relevant to Package Maintainers

New since 5.6:

- Optionally link against `libtcmalloc.so` which comes with Google's perftools, to fix issues where glibc won't give memory back to the OS. Use via the CMake options `ENABLE_TCMALLOC` and `TCMALLOC_LIB_DIR`.

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

Complete revision history [available on GitHub](https://github.com/Beep6581/RawTherapee/commits/5.8).
