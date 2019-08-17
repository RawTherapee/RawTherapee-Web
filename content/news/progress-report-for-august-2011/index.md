---
title: "Progress report for August 2011"
date: 2011-09-01T01:58:00+00:00
author: DrSlony
Tags:
- Documentation
- Versions
---



The following changelog details a list of items that have been fixed
and/or implemented in the development branch of RawTherapee from the
31st of July till the 31st of August, 2011:


  - Color probes and clipping indicators were using the working color
    space values instead of the output color space ones. Also RT would
    fallback to using the sRGB color space for the processed photos if
    the chosen output profile not match the working profile.
    [Issue 889](http://code.google.com/p/rawtherapee/issues/detail?id=889).
  - Fixed a bug where the queue's output file format would change to the
    format you used in the direct save dialog if you used it while the
    queue was populated.
    [Issue 890](http://code.google.com/p/rawtherapee/issues/detail?id=890)
  - Default theme set to 25-Gray-Gray to satisfy presumed standard
    viewing conditions.
    [Issue 373](http://code.google.com/p/rawtherapee/issues/detail?id=373)
  - Fixed bug with the file browser thumbnail showing an incorrect crop
  - Fixed Windows bug where if you replaced one raw with another, of the
    same name, RT would continue showing the old one's thumbnail.
    Required clearing your thumbnail cache.
    [Issue 893](http://code.google.com/p/rawtherapee/issues/detail?id=893)
  - Fixed bug where the thumbnails in the file browser would not refresh
    when the "Show EXIF info" button was toggled. Improved stability.
    Fixed skewed thumbnails.
    [Issue 898](http://code.google.com/p/rawtherapee/issues/detail?id=898)
  - Performance improvements when adding many files to the queue.
    [Issue 900](http://code.google.com/p/rawtherapee/issues/detail?id=900)
  - Fixed a bug where dotted lines would appear when using a non-zero
    Green Equilibration value.
    [Issue 904](http://code.google.com/p/rawtherapee/issues/detail?id=904)
  - Fixed the direct save dialog, it would try saving the photo even if
    no filename was specified to a file with just the extension, e.g.
    ".tif"
  - Fixed a bug with the histogram behaving oddly when resized. Also
    added histogram channel buttons.
    [Issue 909](http://code.google.com/p/rawtherapee/issues/detail?id=909)
  - "Clarity and sharpening" renamed to "Local sharpening" and the
    tool's panel was cleaned up.
    [Issue 927](http://code.google.com/p/rawtherapee/issues/detail?id=927)
  - The last used directory will be opened when you use the custom ICC
    profile file open dialog.
    [Issue 911](http://code.google.com/p/rawtherapee/issues/detail?id=911)
  - Removed oobsolete and duplicate tools from the toolbox.
  - Added F2 shortcut key for renaming photos.
    [Issue 905](http://code.google.com/p/rawtherapee/issues/detail?id=905)
  - Fixed a bug causing the preview to go black or white when changing
    to a default profile before the first edit.
    [Issue 925](http://code.google.com/p/rawtherapee/issues/detail?id=925)
  - Added option to have a square detail window (smaller than the
    rectangle, therefore faster).
    [Issue 918](http://code.google.com/p/rawtherapee/issues/detail?id=918)
  - RT will no longer re-demosaic the photo when you go back in the
    history panel. It will only do that if you make changes in the Raw
    tab.
    [Issue 923](http://code.google.com/p/rawtherapee/issues/detail?id=923)
  - Custom white balance value is stored and recalled when the "custom"
    white balance setting is used again
  - Fixed RT from crashing when opening a photo with non-linear curves
  - Fixed RT from crashing when opening photos in a certain way when
    using auto-white balance.
    [Issue 929](http://code.google.com/p/rawtherapee/issues/detail?id=929)
  - Fixed dcraw color matrices for Fuji X100 and Sony A77.
    [Issue 930](http://code.google.com/p/rawtherapee/issues/detail?id=930)
  - Custom profile builder will generate a baeline postprocessing
    profile when run manually, but will not run during a partial-paste
    on photos that already have a postprocessing profile (ie. photos
    that have been edited).
    [Issue 941](http://code.google.com/p/rawtherapee/issues/detail?id=941)
  - Panning acceleration when panning the preview image, so that high
    resolution photos can be panned from side to side in one mouse
    movement, needing only one regeneration of the preview.
    [Issue 945](http://code.google.com/p/rawtherapee/issues/detail?id=945)
  - Chrominance noise reduction multiplier increased, fixing a bug where
    said noise reduction would work very poorly.
    [Issue 719](http://code.google.com/p/rawtherapee/issues/detail?id=719)
  - Fixed bug where "profile applied gamma" would not toggle a preview
    refresh
  - Automatic ICC profile detection.
    [Issue 938](http://code.google.com/p/rawtherapee/issues/detail?id=938)
  - Fixed a bug where RT would only auto-rotate raw files and not the
    corresponding JPG files if both were shot using the "RAW+JPG" mode
    with the camera vertically-oriented.
    [Issue 125](http://code.google.com/p/rawtherapee/issues/detail?id=125)
  - New feature to blend LittleCMS highlight values with those of the
    dcraw/RT simple matrices.
    [Issue 951](http://code.google.com/p/rawtherapee/issues/detail?id=951)
  - Various translation updates
  - We switched to using Google Docs for the RawTherapee Manual and
    translations of it. It should make real time collaboration easier
    without forcing the user to install any extra software.
    [Issue 939](http://code.google.com/p/rawtherapee/issues/detail?id=939)

