---
title: "RawTherapee v5.8"
date: 2020-02-04T08:00:00+01:00
draft: false
version: "5.8"
linux_appimage: "https://rawtherapee.com/shared/builds/linux/RawTherapee_5.8.AppImage"
linux_binary_32: ""
linux_binary_64: ""
windows_binary: "https://rawtherapee.com/shared/builds/windows/RawTherapee_5.8.exe"
windows_xp_binary: ""
mac_binary: "https://rawtherapee.com/shared/builds/mac/RawTherapee_5.8.dmg"
source_code: "https://rawtherapee.com/shared/source/rawtherapee-5.8.tar.xz"
---

RawTherapee 5.8 has been released\!

## Windows Build Repackaged

We found an issue with the original 5.8 Windows installer, it was missing the Profiled Lens Correction (Lensfun) database, so there is now a new installer from 2020-02-06 which includes this database. If you downloaded RawTherapee 5.8 for Windows previously, please download the new build and re-install.

## macOS Installation Instructions

To install RawTherapee, download the build and open the `.dmg` file, then drag the RawTherapee app onto the Applications folder.

Attention macOS 10.15 Catalina users: RawTherapee needs to be "authorized" to allow it to open photographs on your disk. To authorize it:

1. Click "Go" &gt; "Go to Folder…⇧⌘G" (Command-Shift-G), and go to `/bin`
1. Drag `sh` into the "Full Disk Access" pane under the "Privacy" tab in the "Security & Privacy" control panel in "Apple menu" &gt; "System Preferences".

## Linux Installation Instructions

Software should be installed through your distribution's package manager.

If RawTherapee&nbsp;5.8 is not yet available in your package manager, you can use the AppImage:

1. Download it.
1. Make it executable:
`chmod u+x RawTherapee_5.8.AppImage`
1. Run it:
`./RawTherapee_5.8.AppImage`

## Screenshot

{{< figure src="rt58_amanita_muscaria_capture_sharpening.jpg" link="rt58_amanita_muscaria_capture_sharpening.jpg">}}

## New Features

- Automatically recover detail lost to lens blur (diffraction) using the new Capture Sharpening tool, located in the "Raw" tab. It takes place right after demosaicing, and as it works in linear space it is not prone to haloing. Capture Sharpening in combination with Post-Resize Sharpening allows for detailed and crisp results.
- CR3 support: image data is decoded so you can process your raw files, but metadata is not supported yet. If you have an ICC or DCP input profile for your CR3-producing camera, you will need to point RawTherapee to it manually (Color tab &gt; Color Management &gt; Input Profile &gt; Custom).
- Improvements of various camera models (new DCP dual-illuminant input profiles, raw crops, white levels, etc.), speedups and optimizations to various tools, better memory management, various bug fixes. See the git log for details.

RawTherapee and other open-source projects require access to sample raw files from various camera makes and models in order to support those raw formats correctly. You can help by submitting raw files to RPU: https://raw.pixls.us/

## News Relevant to Package Maintainers

New since 5.7:

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
