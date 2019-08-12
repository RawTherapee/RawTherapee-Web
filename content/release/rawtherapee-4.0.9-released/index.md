---
title: "RawTherapee 4.0.9 released"
date: 2012-06-04T19:50:00+00:00
author: DrSlony
Tags:
- Downloads
- Versions
---



RawTherapee 4.0.9 is out\!

Builds should be ready within a day or two. Once they are, get them from
the [Downloads](/downloads) section or using your operating system's
package manager (source code tarball available from our [Google
Code](http://code.google.com/p/rawtherapee/downloads/list "Link to our Google Code download page for the source code")
page).

Read below to find out more about what's new.

{{< figure src="rt409_lago_di_braies_702.jpg" alt="Screenshot of RawTherapee-4.0.9" link="rt409_lago_di_braies.jpg" >}}


# New features

* Support for Adobe LCP lens correction profiles
* Program plugger for Windows, to automatically find and be able to open right-clicked photos with popular photography programs.
* Support of dual illuminant DCP profiles
* Support for new cameras in addition to those already supported by dcraw:
  - Nikon D800
  - Canon EOS 5D Mark III
* New camera DCP profiles:
  - Nikon D5100
  - Nikon D7000
In addition to these new features, as usual there were numerous bug-fixes, and speed and stability improvements.


Work is well underway on a number of other features, among them improved
[noise reduction](http://rawtherapee.com/forum/viewtopic.php?f=1&t=3793#p27341),
XMP and Lua support. In addition to that we're plugging memory leaks and
working towards making RT run faster and use less memory. Stay tuned\!


# Caveats

  - Default raw and non-raw processing profiles have changed. If you
    have used any version of RawTherapee older than 4.0.9, you must go
    to Preferences \> Image Processing and select new default image
    processing parameters. It is recommended that you use "Default" for
    raw files and "Neutral" for image files.
  - Risk of PP3 data loss - beware when running multiple RT versions  
    RawTherapee cleans up obsolete or invalid tags from active PP3
    files. The tag cleanup process is run in three situations:  
    1.  When you affect the PP3 file in any way, e.g. by tagging a
        photo,
    2.  When you select another folder in the File Browser tab,
    3.  When you exit RawTherapee (equivalent to leaving the open
        album).
    This means that a more recent version of RawTherapee will delete
    obsolete tags which may have been used by an older version, and vice
    versa - if you use an old version of RawTherapee to browse photos
    edited with a newer version, it will delete the tags introduced in
    the new version. This issue is being worked on and future versions
    of RawTherapee will support XMP sidecar files with concurrent
    embedded profile versions.  
    http://code.google.com/p/rawtherapee/issues/detail?id=1335
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
    Space profiles are not the same. A workaround is to set them to the
    same values to ensure the preview accurately reflects the final
    rendered output.

