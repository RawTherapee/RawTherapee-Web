---
title: "RawTherapee v4.1"
date: 2014-05-21T14:31:00+00:00
author: DrSlony
draft: false
version: "4.1"
linux_appimage: ""
linux_binary_32: ""
linux_binary_64: ""
windows_binary: "https://rawtherapee.com/shared/builds/windows/RawTherapee_WinVista_64_4.1.1.zip"
windows_xp_binary: "https://rawtherapee.com/shared/builds/windows/RawTherapee_WinXP_32_4.1.zip"
mac_binary: "https://rawtherapee.com/shared/builds/mac/RawTherapee_OSX_10.7_64_4.1.zip"
source_code: ""
---


Spring is here (or autumn, for those on the other side of the planet),
and it's a fantastic time to capture nature in its fresh,
luminescent-green light (or that intense, golden-red autumn light\!),
and how better to develop your raw photos than with RawTherapee
4.1-stable\!

YES\! It's been a long journey since the last version we officially
called *stable*, version 3.1. A few years have passed, many new tools
and features have been added, a million little bugs were squashed, and
now it has arrived\!

{{< figure src="rt_splash_4.1.png" >}}


Be sure to read [RawPedia](https://rawpedia.rawtherapee.com/) to understand how each tool works to make the most of it.

In order to use RawTherapee efficiently you should know that:

- You can scroll all panels using the mouse scroll-wheel.
- To change slider values or drop-down list items with the mouse scroll-wheel, hold the Shift key. This is so that you can safely scroll the panels without accidentally changing a slider or other tool setting.
- All curves support the Shift and Ctrl keys while dragging a point. Shift+drag makes the point snap to meaningful axes (top, bottom, diagonal, other), while Ctrl+drag makes your mouse movement super-fine for precise point positioning.
- There are many keyboard shortcuts which make working with RawTherapee much faster and give you greater control, make sure you familiarize yourself with them on RawPedia's [Keyboard Shortcuts](http://rawpedia.rawtherapee.com/Keyboard_Shortcuts) page\!



## New features

Since 4.0.12

- [Pipette](http://rawpedia.rawtherapee.com/General_Comments_About_Some_Toolbox_Widgets#Pipette "RawPedia - Pipette") tool for curves.
- Support for floating-point [HDR raw DNG](https://github.com/jcelaya/hdrmerge "HDRMerge project page") images.
- Enhanced look for all tools (panel background).
- Enhanced look for [crop](http://rawpedia.rawtherapee.com/Crop "RawPedia - Crop") guides, zoom guides  [straightening line](http://rawpedia.rawtherapee.com/Lens/Geometry#Rotate "RawPedia - Straightening Line"), [Navigator panel](http://rawpedia.rawtherapee.com/The_Image_Editor_Tab#Navigator "RawPedia - Navigator panel") and detail windows.
- Enhanced [focus mask](http://rawpedia.rawtherapee.com/The_Image_Editor_Tab#Focus_Mask "RawPedia - Focus Mask").
- Skin-tones targetting for [Contrast by Detail Levels](http://rawpedia.rawtherapee.com/Contrast%20by%20Detail%20Levels "RawPedia - Contrast by Detail Levels") tool.
- "None" [demosaicing](http://rawpedia.rawtherapee.com/Demosaicing "RawPedia - Demosaicing") method to show the raw image without demosaicing.
- New algorithm for orange, yellow, cyan, purple and magenta in the [Black-and-White](http://rawpedia.rawtherapee.com/Black-and-White "RawPedia - Black-and-White tool") tool.
- Set the cache and config [paths](http://rawpedia.rawtherapee.com/File%20Paths "RawPedia - File Paths") using environment variables.
- JPEG subsampling parameter in the [command-line interface](http://rawpedia.rawtherapee.com/Command-Line_Options "RawPedia - Command-line Interface").
- The opened/closed state of the left and right panels of the File Browser tab is now remembered between sessions.
- RawTherapee's window size and position are remembered between sessions.
- When cropping, click anywhere without dragging to clear crop.
- Added 'no wait' option (-w) for [command-line](http://rawpedia.rawtherapee.com/Command-Line_Options "RawPedia - Command-line Interface") (Windows
- only).
- [dcraw](http://www.cybercom.net/~dcoffin/dcraw/ "dcraw") 9.20 Revision: 1.461.
- New or improved support for:
    - Canon EOS 5D Mark II
    - Canon EOS 5D Mark III
    - Canon EOS 6D
    - Canon EOS 40D
    - Canon EOS 50D
    - Canon EOS 60D
    - Canon EOS 70D
    - Canon EOS 600D/Rebel T3i/Kiss X5
    - Canon EOS 650D/Rebel T4i/Kiss X6i
    - Canon EOS 1200D/Rebel T5/Kiss X70
    - Canon EOS-M
    - Canon PowerShot G1 X Mark II
    - Canon PowerShot S120
    - Fujifilm S1
    - Hasselblad CFV-50
    - Nikon 1 V3
    - Nikon D4s
    - Nikon D3300
    - Nikon D5300
    - Nikon D7000
    - Olympus E-M10
    - Olympus E-PM2
    - Panasonic DMC-GH3
    - Panasonic DMC-GH4
    - Panasonic DMC-GM1
    - Panasonic DMC-GX7
    - Panasonic DMC-LF1
    - Panasonic DMC-ZS40/Panasonic DMC-TZ60
    - Panasonic DMC-ZS41/Panasonic DMC-TZ61
    - Pentax K10D
    - Pentax K-3
    - Phase One IQ180/IQ280
    - Phase One IQ260
    - Phase One IQ260
    - Phase One P20/P20+
    - Phase One P21/P21+
    - Phase One P25/P25+
    - Phase One P30/P30+
    - Phase One P40+/IQ140
    - Phase One P45/P45+
    - Phase One P65+/IQ160
    - Samsung NX30
    - Sony ILCE-7R
    - Sony ILCE-3000
    - Sony ILCE-5000
    - Sony ILCE-6000
    - Sony NEX-5N
    - Sony SLT-A77
    - Sony SLT-A99/Sony SLT-A99V
