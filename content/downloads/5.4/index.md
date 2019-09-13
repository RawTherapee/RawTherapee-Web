---
title: "RawTherapee v5.4"
date: 2018-03-20T13:34:00+00:00
author: DrSlony
draft: false
version: "5.4"
linux_appimage: "https://rawtherapee.com/shared/builds/linux/RawTherapee-releases-5.4.AppImage"
linux_binary_32: ""
linux_binary_64: ""
windows_binary: "https://rawtherapee.com/shared/builds/windows/RawTherapee_5.4_WinVista_64.zip"
windows_xp_binary: ""
mac_binary: "https://rawtherapee.com/shared/builds/mac/RawTherapee_OSX_10.9_64_5.4.zip"
source_code: "https://rawtherapee.com/shared/source/rawtherapee-5.4.tar.xz"
---


RawTherapee 5.4 has been released\!

{{< figure src="rt_splash_5.4.png" >}}

### New Features

- New default processing profiles, now the default look for raw photos closely matches the out-of-camera look with regard to tones and includes lens distortion and vignetting correction.
- New histogram matching tool, to have RawTherapee automatically adjust the image for you to match the out-of-camera look with a single click of a button.
- New HDR Tone Mapping tool to compress the light in scenes with a high dynamic range, allowing you to show details in both shadows and highlights in a realistic way.
- New Local Contrast tool to boost clarity using a simple interface.
- New color toning method L\*a\*b\- Color Correction Grid.
- New RCD demosaicing algorithm to minimize artifacts even with artificial lighting and strong chromatic aberration.
- New thumbnail overlay icons in the File Browser and Filmstrip to help you distinguish normal images from HDR and Pixel Shift ones.
- Added support for showing out-of-gamut areas based on the output profile.
- Added support for reading and writing metadata and ICC profiles to and from PNG images.
- Added support for processing Sony Pixel Shift ARQ raw files - make sure that the ARQ extension is enabled in Preferences \> File Browser \> Parsed Extensions.
- Create Sony ARQ raw files using https://github.com/agriggio/make\_arq
- Added support for saving 32-bit floating-point TIFFs clamped to \[0;1\].
- Added profiled chromatic aberration correction support using Lensfun.
- More tools now have an on/off switch.
- The user interface is cleaner, with all power-house tools moved into a new "Advanced" tab to prevent slider-shock to newcomers.
- The Metadata tab now lets you choose whether you want to copy metadata unchanged, edit metadata or strip metadata when saving images. Now you can also make metadata changes in batch mode.
- The choice of whether the main histogram should display information using the working profile or the output profile is now available from the Editor tab's top toolbar.
- The Crop tool's aspect ratio now defaults to that of the image, and RawTherapee automatically zooms-to-fit the crop once it's placed.
- RGB input-type ICC profiles can now be used as output profiles.
- The saved reference image for profiling (created from within the Color Management tool) now contains metadata.
- PNG and compressed TIFF images make use of better compression.
- Shortcut key changes: Zoom-to-fit the crop using "f", fit the whole image using "Alt+f".

There were several hundred commits optimizing processing speed and memory usage as well as bug fixes and code refactoring, though the details of these are too arcane to list here. The effort involved thousands of developer-hours.

RawTherapee and other open-source projects require access to sample raw files from various camera makes and models in order to support those raw formats correctly. You can help by submitting raw files to RPU: <https://raw.pixls.us/>


## News Relevant to Package Maintainers

No changes since 5.3.

- To get the source code, either clone from git or use the tarball from <http://rawtherapee.com/shared/source/> . Do not use the auto-generated GitHub release tarballs.
- Requires GTK+ version \>=3.16, though \>=3.22 is recommended.
- RawTherapee 5 requires GCC-4.9 or higher, or Clang.
- Do not use `-ffast-math`, it will not make RawTherapee faster but will introduce artifacts.
- Use `-O3`, it will make RawTherapee faster with no known side-effects.
- For stable releases use `-DCACHE_NAME_SUFFIX=""`
- For development builds and release-candidates use `-DCACHE_NAME_SUFFIX="5-dev"`


## News Relevant to Developers

See [CONTRIBUTING.md](https://github.com/Beep6581/RawTherapee/blob/dev/CONTRIBUTING.md).


Complete revision history available on
[GitHub](https://github.com/Beep6581/RawTherapee/commits/5.4).
