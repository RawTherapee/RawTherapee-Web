---
title: "RawTherapee 4.0.8 released"
date: 2012-04-01T23:43:00+00:00
author: DrSlony
Tags:
- Downloads
- Versions
draft: false
version: ""
linux_binary: ""
windows_binary: ""
mac_binary: ""
source_code: ""
---



RawTherapee 4.0.8 is out\!

Get it from the [Downloads](/downloads) section or using your operating
system's package manager (source code tarball available from our [Google Code](http://code.google.com/p/rawtherapee/downloads/list "Link to our Google Code download page for the source code") page),
or read below to find out more about what's new.


{{< figure src="rt408_flower1_702.jpg" alt="Screenshot of RawTherapee-4.0.8 processing a photo of a flower" link="rt408_flower1.jpg" >}}

# New features


  - Support for loading, saving, copying and pasting partial profiles
  - Support for using clipless DCP input profiles
  - Subdirectory support for ICC and DCP profiles
  - Support for RGBLF preview modes in the Before|After view
  - Automatic support for CaptureOne and hacked Nikon ICC profiles
  - New input color profiles (DCP and/or ICC) for the following cameras:
      - Canon EOS 7D
      - Canon EOS 60D
      - Canon EOS 40D
      - Canon EOS 400D
      - Canon EOS 550D
      - Canon Powershot G12
      - Nikon D50
      - Nikon D300
      - Nikon D3000
      - Olympus E-1
      - Pentax K10D
      - Sony A900


In addition to these new features, as usual there were numerous
bug-fixes, and speed and stability improvements.


Work is well underway on a number of other features, among them improved
[noise
reduction](http://rawtherapee.com/forum/viewtopic.php?f=1&t=3793#p27341),
XMP and Lua support. In addition to that we're plugging memory leaks and
working towards making RT run faster and use less memory. Stay tuned\!


# Caveats


  - Memory requirements
    Please read the blog entry on [maximizing memory
    efficiency](blog/maximizing-memory-efficiency)
  - Differences between the preview and the output image
    The color-managed preview in RawTherapee is (and has always been)
    based on image data in the Working Space profile. Although the
    actual preview is rendered using a monitor profile (or sRGB profile,
    if the monitor profile is not specified), it does not reflect the
    Output Profile & Output Gamma settings. This can lead to a slightly
    different output rendering when Working Space profile and Output
    Space profiles are not the same. A workaround is to set them to the
    same values to ensure the preview accurately reflects the final
    rendered output.
  - For generic use in an sRGB workflow when the output target is
    web-based image display, it is recommended to use the default values
    of the Color/ICM toolset (Working Profile = sRGB, Output Profile =
    RT\_sRGB).
  - Future releases of RawTherapee are planned to support a more
    comprehensive color-managed preview that will allow proofing with
    accurate visualization of the final output render based not only on
    the working space and monitor profiles, but also on the
    user-selected Output Profile and Output Gamma.
