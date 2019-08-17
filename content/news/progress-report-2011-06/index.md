---
title: "Progress report"
date: 2011-06-19T03:39:00+00:00
author: DrSlony
Tags:
- Documentation
- Versions
- RT 3.0
- RT 3.1
---

It is our pleasure to inform you of the progress made in RawTherapee
since the last report\!

We have repeatedly decided to push back the release of the version we
would call 3.0 in order to deliver a program that you can expect the
best quality and optimal speed from, one you can entrust your photos
with and rely upon. During this time many<span id="lead_end"></span>
improvements have been made, much code has been refactored, memory leaks
plugged and stability improved. A large part of this was possible
because of the feedback we received from you, so if you have any good
ideas on how to improve RawTherapee or if you experience instability or
other bugs, please take the time to first [read this short
guide](http://www.rawtherapee.com/forum/viewtopic.php?t=1428) and then
report your issue either in [our
forum](http://www.rawtherapee.com/forum/viewforum.php?f=3) or in [our
Google Code page](http://code.google.com/p/rawtherapee/issues/list).

What follows is a summary of the more interesting additions and
improvements from our team of developers. "Branch\_3.0" will become
"**RawTherapee version 3.0**" once ready, and the "default" branch will
become "RawTherapee version 3.1" once ready. **These additions and
improvements apply to both branch\_3.0 and default\!**

  - A new and powerful hue, saturation and value manipulation tool,
  - Speed and quality improvements to all the tools available,
  - More keyboard shortcuts,
  - New dual-monitor interface layout,
  - Automatic and manual chromatic aberration removal tools for pre and
      post-demosaicing,
  - Purple fringe removal tool,
  - Cosmetic interface improvements for low resolution displays,
  - Possibility to ignore a photo's color profile,
  - Auto white balance improved to ignore overexposed areas,
  - Preference to overwrite existing output file or write the new one
      under a different name if one already exists,
  - Ability to change the cropped off area's opacity and color,
  - Thumbnail quality improved,
  - Thumbnail loading speed improved,
  - In single tab mode, the file browser follows the currently open
      photo in the editor tab,
  - New preview size button: "fit"
  - International character support in filenames and metadata,
  - Hot and dead pixel correction filter,
  - Dark frame subtraction,
  - Autoexposure behaviour corrected in relation to highlight
      reconstruction,
  - Highlight recovery amount and threshold sliders,
  - Exposure slider range increased,
  - Ability to save a 16 bit TIFF image for color profiling,
  - Interface enhancement: right-clicking over a section title expands
      that section and hides the others,
  - Shadow and highlight clipping indicators use luminance instead of R,
      G or B channel values,
  - High quality shadows/highlights filter has been sped up,
  - New crop ratios,
  - Ability to resize the photo to fit within a "bounding box",  
  - The non-100% preview image of the photo in the editor has been made
      smoother and gamma-corrected,
  - Version number displayed in title bar,
  - The batch queue is automatically saved in case of a crash,
  - Details of the RawTherapee version as well as the build environment
      are available if you click on Preferences \> About \> Version. Copy
      and paste this whole chunk of text whenever reporting a bug.
  - GUI element placement improved,
  - Fluid GUI elements scale better,
  - Dcraw updated,
  - EXIF updates,
  - Translations updated,
  - Fast file access with memory mapped files
  - Default compilation type: release
  - New user interface themes,
  - User interface made nicer, especially in Windows (clearlooks),
  - User interface icons updated,
  - Numerous memory leaks plugged,
  - Numerous speed & stability improvements.

Furthermore, the following additions and improvements are applied only
to the default branch, which will become **RawTherapee version 3.1**
when ready:

  - Floating point pipeline,
  - LCMS2,
  - New highlight recovery method "blend",
  - New highlight recovery method "color propagation" (replaced old
      method of the same name, the new one is better and faster),
  - Better handling of (over)saturated colors,
  - Input and output color profile handling more powerful,
  - Color matrices converted to Bradford adapted D50 reference space,
  - Flat field correction,
  - Raw white point sliders,
  - Individual black level sliders for the red, blue and both (if
      available) green channels,
  - Free output gamma sliders,
  - Ability to rate images using color labels,
  - Command line mode greatly enhanced: ability to load a single image
      or a whole directory, ability to process a list of files using a
      chosen pp3 profile
  - To reduce the overhead for programmers and to improve stability a
      class 'LUT' has been added which functions as a look up table.
  - Ability to only partially apply a PP3 profile,
  - Possibility to play sounds when completing lengthy operations
      (Windows only),
  - Ability to copy the original raw metadata (XMP) over to the
      processed photograph files,
  - Automatic monitor color profile detection,
  - Opening of processed image with default viewer (F5, SHIFT+F5,
      CTRL+F5; Windows only),
  - New filtering toolbar in the file browser,
  - Greyscale encoded and output color profile aware clipping
      indicators,
  - Configurable layout of the editor window,
  - Numerous memory leaks plugged,
  - Numerous speed & stability improvements.

