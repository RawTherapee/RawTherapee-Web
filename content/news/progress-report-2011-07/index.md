---
title: "Progress report for July 2011"
date: 2011-08-03T02:01:00+00:00
author: DrSlony
Tags:
- Versions
---



The following changelog details a list of items that have been fixed
and/or implemented in the development branch of RawTherapee from the
19th of June till the 31st of July, 2011:<span id="lead_end"></span>


  - Fixed issue when using false color suppression on very overexposed
    photos where whites turned grey.
  - Threading improved.
  - Case-insensitive "find" toolbar in file browser to search by
    filename. Ability to display said toolbar in two rows.
  - Stability improvements.
  - Fixed numerous bugs that made RawTherapee freeze for short periods
    of time.
  - The file browser context menu has been rearranged into groups,
    customizable through the preferences panel.
  - RawTherapee color themes fixed to work well in Ubuntu 11.04 (GTK3).
  - Fixed error where large positive Exposure Compensation values along
    with large negative Black values caused light regions to turn black.
  - Translation updates: French, German, Catalan, Czech, Russian,
  - New highlight reconstruction algorithm, faster and better than the
    old one.
  - File browser filters: (Not) Saved, (Not) Edited.
  - The Amaze demosaicing algorithm no longer produces artifacts in
    white areas.
  - Windows: mute button for RawTherapee sound notifications, and RT
    automatically appears in the Windows Mixer.
  - Further floating point conversions.
  - Compiler warnings suppressed.
  - Executable renamed from "rt" to "rawtherapee".
  - JPEG images in the CMYK color model are ignored by RT.
  - New sharpening methods: Gradient Sharpening (border), and
    Microcontrast (texture). Both available under Detail \> Clarity and
    Sharpening.
  - Curve histograms no longer show garbage when opening a raw file.
  - Extended support in various filters for partial profile paste.
  - New CMAKE
    "[BUNDLE](http://code.google.com/p/rawtherapee/issues/detail?id=184#c48 "Google Code issue 184 - CMAKE BUNDLE option")"
    option, -DBUNDLE=ON
  - Selecting an aspect ratio in the crop panel automatically enables
    "use fixed ratio".
  - Removed RAWZOR.
  - Various icons replaced.
  - PP3 sidecar files were unnecessarily triggering RawTherapee
    directory monitoring events which caused RT to occasionally freeze.
  - RT was using the "fast" demosaicing algorithm even when another
    algorithm was selected as the default one in your PP3 profile. It
    would only refresh the preview to your chosen demosaicing algorithm
    when you used certain tools that forced the preview to get
    re-rendered. This should now be fixed.
  - Change of mouse cursor from an open hand to a crosshair.
  - Windows: fixed sorting of disks in "Places", should now be sorted
    A-Z.
  - Windows: Automatic language detection.
  - Fixed cropping to work properly once more from thumbnail level in
    the File Browser tab.
  - Batch queue context menu fixed to not disappear.
  - New default PP3 profiles (Neutral, default(ISO), BW, Tuned, Natural,
    Punchy).
  - Update to
    [dcraw](http://www.cybercom.net/~dcoffin/dcraw/ "Dave Coffin's dcraw")-9.10
  - Fixed bug where thumnails would appear too dark when "Highlight
    Recovery" was enabled.
  - Fixed a bug where the file extension was not appended when saving
    the image directly, bypassing the queue.
  - Prevent RT from crashing when encountering a corrupt raw file.
  - Fixed articfacts when using exposure saturation on dark noisy Canon
    images.
  - Fixed RL Deconvolution from causing artifacts to appear when using
    certain slider values (e.g. 5 iterations) or a negative lightness
    channel.
  - RawTherapee tagged 4.0.0 (no we haven't released RawTherapee 4.0
    yet, this is a development version, but we decided to call it 4.0 as
    so much has changed from 3.0.0).

  


As always, you can find nightly development builds of RawTherapee in our
[downloads
section](http://rawtherapee.com/downloads "RawTherapee Downloads section"),
along with the latest stable version, 3.0.

