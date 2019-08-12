---
title: "RawTherapee V2.1 released"
date: 2007-05-04T00:00:00+00:00
author: dualon
Tags:
- RT 2.1
---


The main changes are:  

  - Tone curve and Luminance Curve editors implemented
  - Sharpening now entails much fewer sharpening halos
  - Improved response to color boost and luminance curve adjustments
  - Much better highlight handling
  - Auto white balance algorithm has been replaced
  - A new (faster) demosaicing algorithm, HPHD, is available and it is
    now the default
  - Hideable history and file browser panels
  - New cameras are supported: Fuji SuperCCD, D1X and raw files with the
    Canon hack
  - Thumbnail size in file browser is now adjustable in the Preferences
    dialog

More details about some changes:  

  - _Sharpening_: in this release
    you can set a higher amount of sharpening with less artifacts. The
    postprocessing profiles have been updated as well to apply more
    sharpening. If you think the images are oversharpened, you can
    always edit/change the default profiles.
  - _Color boost_ and
    _luminance curve_
    enhancements: you dont have to be as careful with these controls as
    before. The colors do not get oversaturated so easy in you adjust
    color boost and the image does not get too bright as easy as before
    if you increase luminance brightening.
  - Imroved _highlight handling_:
    an other highlight recovery method has been implemented (thanks to
    Dave Coffin and Cyril Guyot). This new method called 'Luminance
    recovery') does not recover colors in the overexposed areas, but it
    recovers the luminance channel more reliably. It is much faster than
    the existing one, and causes no false colors, so I decided to enable
    it in all of the built-in profiles. If your photo is overexposed
    only moderately, the old method (called 'Color propagation') gives
    better results.
  - The new demosaicing method,
    _HPHD:_ This method has even
    better resolution compared to the existing algorithm, EAHD. It is
    also at least twice as fast, and is parallelizable (so on dual core
    processors it is even faster), and has better noise pattern. HPHD is
    now the default demosaicing method in RawTherapee. It also has some
    drawbacks compared to EAHD: with cameras having a weak antialias
    filter it entails moire and zipper effect a bit more often. If you
    are not pleased with its quality, you can switch back to EAHD in the
    Preferences dialog.

Please test the _crisp_ profile
as well and give me feedback if you find it oversharpened or
oversaturated, and indicate if
_crisp_ could be used as the
default profile in future versions.  
  
If you like RawTherapee please do not forget about the
[donation](http://www.rawtherapee.com/donation.html) (it is only $5\!).

