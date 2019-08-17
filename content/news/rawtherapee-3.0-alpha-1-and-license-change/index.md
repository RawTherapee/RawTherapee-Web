---
title: "RawTherapee 3.0 alpha 1 and license changes"
date: 2010-01-04T22:05:00+00:00
author: dualon
Tags:
- Community
- RT 3.0
---



The first alpha version of RawTherapee 3.0 is available for download.
Note that this is not a feature complete version. In V3.0 both major  
GUI/workflow and algorithm changes are planned. This alpha version
demonstrates the new, much more efficient GUI, but it does not contain  
any algorithmic changes yet.

The most significant changes in the GUI are
the following:

  - multi-tab interface
  - the real batch processing support arrived: select multiple images
    and adjust them together (the multi-adjust behavior of some
    parameters is selectable in the preferences dialog: they can be
    either additive or absolute)
  - completely re-written editor: preview and detail view are now gone.
    The main image view can be magnified as required, and only the
    necessary part of the image will be re-calculated. There is a small
    navigator, too, and infinitely many detailed views can be opened to
    investigate fine details.
  - 16 bit thumbnails (an option, takes double disk space)
  - before/after view in the editor

The only change in the algorithms is:

  - the behavior of the exposure controls changed. The "exposure"
    parameter is what was called "brightness" in previous versions. The
    "brightness" parameter is now a real brightness control, that shifts
    the histogram (of course with highlight/shadow protection)

Roadmap of algorithm changes planned for V3.0 (approximately in sequence
of implementation):

  - new curve editor with parametric curve support
  - per-image selectable demosaicing method + brand new demosaicing
    methods
  - new color denoising method
  - new luminance denoising method
  - automatic C/A correction
  - purple fringing correction
  - perspective correction
  - bad pixel removal

License changes:  
  
I decided to change the license to GPL and thus offer the source code to
the open source community. This does not mean that I stop developing
RawTherapee. I will invest as much time into the development as till
now. I have three motivations for this decision: first, I love playing
with image processing algorithms but I'm not keen on GUI development.
Recently a huge amount of work had to be invested to develop a usable
GUI and I had no time left to play with new algorithms. I hope to
involve some new developers who help me to maintain and enhance the GUI.
The second reason of licence change was that I am very frustrated by the
huge amount of bug reports I can not reproduce (believe it or not, RT is
stable on my PC). I hope that with the open source model some talented
users can identify the problems and fix the bugs. The third (but maybe
the most important) reason of switching to GPL is that our baby reached
the age (10 month old) when he needs his father more and more. I dont
want to disappoint him :). With more developers involved the development
process will hopefully more smooth and wont stop when I am busy.  
  
Some technical details for future developers:

  - The SVN and issue tracker is maintained by google code [here  
    ](http://code.google.com/p/rawtherapee/)
  - The development discussions are running on the forum
  - Patches are to be sent to: patches at rawtherapee dot com
  - RawTherapee consists of the following 3 parts: rtexif: the
    exif/makernote support library. It is quite complete and works well.
    It needs continuous maintenance, for which I have too few time. The
    maintenance means to maintain the exif and makernote tag
    interpretation tables (to follow newest cameras, lenses, etc), for
    example based on the excellent informations found
    [here](http://www.sno.phy.queensu.ca/%7Ephil/exiftool/TagNames/).
  - rtengine: this is the image processing library. It has a quite clear
    calling interface, but the code behind is a bit messy right now,
    since I am in the middle of a cleanup. If there will be several
    developers involved in the project, I would prefer to keep the
    maintenance of rtengine in my hands. The development of this part is
    what I enjoy the most.
  - rtgui: the graphical user interface. This is a very important part
    of RT. If there were enough developers involved, I would be happy to
    hand over the coordination of this part to someone else. Of course,
    I will maintain it, too, if there are no volunteers.

I need help to improve the build system, too (but I want to stick with
cmake -- autotools is painfully slow on windows)

Hardcore linux coders: please accept that windows is a primary platform.
(I use a linux environment for development, too, but the vast majority
of downloads was the windows version)

