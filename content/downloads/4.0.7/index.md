---
title: "RawTherapee v4.0.7"
date: 2012-02-01T22:59:00+00:00
version: "4.0.7"
author: DrSlony
draft: false
linux_appimage: ""
linux_binary_32: ""
linux_binary_64: ""
windows_binary: "https://rawtherapee.com/shared/builds/windows/RawTherapee_WinVista_64_4.0.7.1.zip"
windows_xp_binary: "https://rawtherapee.com/shared/builds/windows/RawTherapee_WinXP_32_4.0.7.1.zip"
mac_binary: ""
source_code: ""
---

RawTherapee 4.0.7 was released on the 1st of February 2012, after two
months of development since the release of the previous 4.0.6 version.
It features new tools, supports more cameras, and has numerous speed and
stability improvements.

## New features

- New RGB curves
- New white balance presets for specific spectra
- New preview modes: red, green, blue, luminosity and Focus Mask (see which areas are in focus)
- New Export Panel with Fast Export Options
- DCRAW updated to 9.12 with added support added for these cameras:
    - Canon PowerShot S100
    - Fujifilm X10
    - Leica V-Lux 3
    - Nikon 1
    - Panasonic DMC-FZ4
    - Panasonic DMC-GX1
    - Samsung NX
    - Samsung NX200
    - Sony NEX-7
- Enhanced color matrices and RT-specific input ICC profiles for the following cameras:
    - Canon EOS 5D
    - Canon PowerShot G10
    - Nikon D3100
- Additional crop ratios
- Additional output ICC profiles
- 1-click neutral setting for exposure values
- Exposure Compensation thumbnail caption and filter option in the file browser metadata filter
- Automatic display of the `RELEASE_NOTES.txt` file on the first run after a RawTherapee upgrade (e.g. 4.0.6 \> 4.0.7)


## Caveats

- Differences between the preview and the output image. The color-managed preview in RawTherapee is (and has always been) based on image data in the Working Space profile. Although the actual preview is rendered using a monitor profile (or sRGB profile, if the monitor profile is not specified), it does not reflect the Output Profile & Output Gamma settings. This can lead to a slightly different output rendering when Working Space profile and Output Space profiles are not the same. A workaround is to set them to the same values to ensure the preview accurately reflects the final rendered output. For generic use in an sRGB workflow when the output target is web-based image display, it is recommended to use the default values of the Color/ICM toolset (Working Profile = sRGB, Output Profile = RT\_sRGB). Future releases of RawTherapee are planned to support a more comprehensive color-managed preview that will allow proofing with accurate visualization of the final output render based not only on the working space and monitor profiles, but also on the user-selected Output Profile and Output Gamma.
- Auto Levels behavior has changed. The new algorithm drives the following parameters:
    - Exposure compensation,
    - Highlight recovery amount & threshold,
    - Black level & shadow compression,
    - RGB brightness,
    - RGB contrast.
- The profiles supplied with RawTherapee were changed to be compatible with the new Auto Levels logic, as in older profiles RGB contrast and brightness were preset to a fixed value. Old Tuned-* profiles have been removed.
- The new Exposure Compensation tag in thumbnail captions and in the file browser filter requires clearing of Rawtherapee's thumbnail cache (see Preferences \> File Browser). If the thumbnail cache is not cleared, exposure compensation values will not be displayed in captions or recognized in filtering for previously browsed images
only.
