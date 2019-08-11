---
title: "RawTherapee 4.0.11 released"
date: 2013-05-29T17:18:00+00:00
author: DrSlony
Tags:
- Downloads
- Versions
---


## RawTherapee 4.0.11 is out\!

4.0.11 includes a number of new features which you can read about below,
but just as importantly it contains a large number of speed improvements
and bug fixes, so we recommend you update straight away\! Builds should
be ready within a day or two. Once they are, get them from the
[Downloads](/downloads) section or using your operating system's package
manager.

The source code tarball is available from our [Google Code](https://code.google.com/p/rawtherapee/downloads/detail?name=rawtherapee-4.0.10.tar.xz "RawTherapee 4.0.10 source code tarball download") page.

Read below to find out more about what's new.

## New features

  - [CIECAM02](http://en.wikipedia.org/wiki/CIECAM02 "Wikipedia article on the Color Appearance Model 2002")
    "Adaptation scene luminosity" now calculated automatically
  - [CIECAM02](http://en.wikipedia.org/wiki/CIECAM02 "Wikipedia article on the Color Appearance Model 2002")
    hot/bad pixel fixer to prevent bright pixels from appearing
  - The
    [Defringe](http://en.wikipedia.org/wiki/Purple_fringing "Wikipedia article on Purple Fringing")
    tool is now able to target a range of specific colors without
    touching others
  - New bundled processing profiles
  - New keyboard shortcuts to apply rank and color labels and a new
    direct popup menu for color labels, all in the File Browser
  - "Profile Fill Mode" button controls whether to replace missing
    processing profile values with default ones or not
  - Keyboard shortcuts to open the next/previous image and to
    synchronize the File Browser strip with the currently opened image
  - New
    [demosaicing](http://en.wikipedia.org/wiki/Demosaicing "Wikipedia article on demosaicing")
    algorithms for noisy photos:
      - LMMSE
      - IGV
  - More zoom levels
  - Redesigned save window
  - New functionality of the minima/maxima control points curves editor,
    see the [RawTherapee
    Manual](http://rawtherapee.com/blog/documentation "RawTherapee documentation page")
  - Support for
    [TIFF](http://en.wikipedia.org/wiki/TIFF/EP "Wikipedia article on TIFF/EP") files
    with [alpha
    channels](http://en.wikipedia.org/wiki/Alpha_channel "Wikipedia article on alpha channels")
  - Support for 32-bit TIFF files
    ([HDR](http://en.wikipedia.org/wiki/High_dynamic_range_imaging "Wikipedia article on high-dynamic-range imaging"))
  - Preferences/Batch processing options: all to 'Add' and all to 'Set'
  - Support for
      - Nikon D5200
      - Nikon D7100
      - Nikon COOLPIX A
      - Panasonic Lumix DMC-G5

\+ Many significant speed improvements and bug fixes.

Refer to the [RawTherapee Manual](http://rawpedia.rawtherapee.com/Main_Page "RawPedia")
for information about these tools and how to use them.

## Caveats

  - Memory requirements  
    Please read the blog entry on [maximizing memory
    efficiency](http://rawtherapee.com/blog/maximizing-memory-efficiency)
  - Differences between the preview and the output image  
    The color-managed preview in RawTherapee is (and has always been)
    based on image data in the Working Space profile. Although the
    actual preview is rendered using a monitor profile (or sRGB profile,
    if the monitor profile is not specified), it does not reflect the
    Output Profile & Output Gamma settings. This can lead to a slightly
    different output rendering when Working Space profile and Output
    Space profiles are not the same. You should set them to the same
    values to ensure the preview accurately reflects the final rendered
    output.

