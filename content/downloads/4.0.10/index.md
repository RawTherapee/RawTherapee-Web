---
title: "RawTherapee v4.0.10"
date: 2013-03-08T05:11:00+00:00
author: DrSlony
draft: false
version: "4.0.10"
linux_appimage: ""
linux_binary_32: ""
linux_binary_64: ""
windows_binary: ""
windows_xp_binary: ""
mac_binary: ""
source_code: "https://rawtherapee.com/shared/source/rawtherapee-4.0.10.tar.xz"
---


## RawTherapee 4.0.10 is out\!

It's been months of hard work, and along the way we made some new
friends who helped make RawTherapee better

Read below to find out more about what's new.

## New features

- Color Appearance Model 2002 ([CIECAM02](http://en.wikipedia.org/wiki/CIECAM02 "Wikipedia article on the Color Appearance Model 2002")) support
- New powerful [Noise Reduction](http://en.wikipedia.org/wiki/Image_noise "Wikipedia article on image noise") tool
- New PP3 processing profiles
- RGB Curve Luminosity mode
- Support for [HDR](http://en.wikipedia.org/wiki/High_dynamic_range_imaging "Wikipedia article on High Dynamic Range Imaging") files in the TIFF 32-bit format
- Support for audio feedback in Linux (see Preferences)
- [Tone mapping](http://en.wikipedia.org/wiki/Tone_mapping "Wikipedia article on tone mapping") using CIECAM02
- [Histogram](http://en.wikipedia.org/wiki/Image_histogram "Wikipedia article on image histograms") backgrounds in curves
- Two tone curves for finer adjustment
- New tone curve modes:
    - Weighted Standard
    - Film-like
    - Saturation and Value Blending
- Support for artistic tone curves in DCP profiles
- New Lab adjustments:
    - CC Curve (chromaticity)
    - CH Curve (chromaticity of hue)
    - LC Curve (luminance of chromaticity)
    - Avoid color shift
    - Red and skin tones protection
    - Black and white toning
- JPEG [subsampling](http://en.wikipedia.org/wiki/Chroma_subsampling "Wikipedia article on chroma subsampling") slider
- Colored bars in curves to aid in adjustment
- [Munsell](http://en.wikipedia.org/wiki/Munsell_color_system "Wikipedia article on the Munsell color system") correction
- Skin tones correction in Vibrance tool
- Keyboard shortcuts:
    - Ctrl+Shift+s to quick-save PP3 in Image Editor tab
    - Ctrl+w to close image tab
    - Alt+s to take a snapshot
    - \+ more, see tooltips and the manual for information
- dcraw 9.17
- New Unsharp Mask (USM) threshold curve widget
- DCP profiles for:
    - Canon EOS 5D Mark III
    - Leaf Aptus 75
    - Nikon D800
    - Olympus E-510
    - Olympus E-520
    - Olympus E-M5i
    - Olympus XZ-1
    - Panasonic DMC-G5
- Auto-fill & auto-crop support when using LCP profiles
- Preview area background color shortcuts in top toolbar

Loads of bugs fixed and speed improvements.

See the revised [manual](http://rawtherapee.com/blog/documentation "Link to the documentation page") for
information about these tools and how to use them\!

## Caveats

- Differences between the preview and the output image.  The color-managed preview in RawTherapee is (and has always been) based on image data in the Working Space profile. Although the actual preview is rendered using a monitor profile (or sRGB profile, if the monitor profile is not specified), it does not reflect the Output Profile & Output Gamma settings. This can lead to a slightly different output rendering when Working Space profile and Output Space profiles are not the same. You should set them to the same values to ensure the preview accurately reflects the final rendered output.
