---
title: "Beta Version released: 2.4beta2"
date: 2008-11-12T13:31:00+00:00
author: dualon
Tags:
- RT 2.4
---



Based on the bug reports of the users many annoying bugs have been
discovered and fixed. There are still some more, but we think it's time
to make beta 2 available for the public.

Bug fixes compared to beta1 are:

  - multiple thumbnails for the same image bug fixed
  - color propagation is back\! However the luminance method is used
    instead in the file browser.
  - proper rights for the "converted" folder under linux
  - history panel cannot be resized after hide/restore fixed
  - send to editor now does not freeze if the app path in invalid
  - duplicate list of extensions in the preferences fixed (you have to
    delete your old options file\!)
  - tiff and rw2 extensions added to the default list of extensions
  - color values under the mouse pointer are now correct
  - directory browser now does not forget its width
  - linear dng/canon sraw is now supported
  - IPTC data in nef files is now detected/parsed
  - several bugs fixed corresponding to the multiple selection in the
    file browser

Known issues (Several users have it but I can
not reproduce them, please test it and post report to the forum if you
found a reproducible scenario for these bugs):

  - some people reported crash when save/save-as is pressed
  - the preview zoom does not work properly (e.g. fit zoom)
  - still no solution on the library dependency problems under older
    linux distributions

