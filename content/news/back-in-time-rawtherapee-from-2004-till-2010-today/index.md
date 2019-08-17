---
title: "Back In Time - RawTherapee From 2004 Till 2010 Today"
date: 2010-09-28T01:22:00+00:00
author: dualon
Tags:
- Versions
---



Apart from numerous minor cosmetic, performance, usability and stability
improvements, quite a few major new features have been and are being
added, but we should start at the beginning - the birth of RawTherapee.

RawTherapee was born in 2004 when Gabor Horvath, from Hungary, bought
his first digital camera. He immediately developed an interest in how
the final JPEG image was obtained from raw data. Being
a PhD student at the time, he had access to
several image processing journals where he found information on relevant
algorithms. By playing with the dcraw code and adding his own
algorithms, he learned that there was much more potential in a raw file
than what contemporary software showed. He learned about other important
steps of the image developing process and consequently his view of how
such an application needs to be implemented evolved over time. The early
versions were therefore sets of ugly hacks, which were the main reason
for keeping the code closed. Only when a large cleanup of the GUI code
was carried out had the code been opened. The second phase involves
cleaning up the engine code which should result in the whole application
coding logic becoming clearer.

The oldest version of the RawTherapee.com website dates back to
2006-09-21, announcing the release of a preview version 1.1. Seven
months later, on 2007-04-04, version 2.0 was released, along with a
donation page. Four months later, a news post announces version 2.2 and
states that of the 35 000 downloads, 80 donations were made. With time
the program matured and gained new features as per user requests. Then,
on Monday the 4th of January 2010, along with the release of version 3.0
alpha 1, Gabor decided to release the source code under a GPL license,
meaning that it was now free for the whole world to read, edit and
improve.

The first task was to upload the source code to a public repository.
Google Code was chosen, <http://code.google.com/p/rawtherapee/>

Once a directory structure was set up and language files were updated,
the code was ready for action. Gabor commited a new curve editor and the
much requested batch feature in April. Wyatt Olson cloned the tree and
was available to accept patches from new developers, so his branch
quickly gained popularity as the one to submit the latest code to. Owing
to its popularity, this branch has been recently incorporated as the
main RawTherapee trunk.

Having been made open source, RawTherapee was now fertile ground for
testing new demosaicing algorithms, and since January 2010 three new
demosaicing algorithms have been added - AMaZE by Emil Martinec
(ejmartin), DCB by Jacek Gozdz and Fast Demosaic by Hombre. Existing
demosaicing algorithms are being improved as well.

Apart from many minor cosmetic, performance, usability and stability
improvements, many new features are being added and existing code
revised. Some of the changes more interesting to our users are: improved
histogram scaling and over/under exposure indicators \[Ilya Popov\],
TIFF LZW compression \[sashavasko\], transition from pp2 to pp3,
perspective correction \[Gabor\], Sony and Pentax EXIF decoding updated
\[ffsup2\], hot pixel removal \[marcin.bajor\], purple fringing and
automatic chromatic aberration removal \[Emil Martinec\], a wavelet
equalizer \[Ilya Popov\], a new way of manipulating the curves called
"cage control" \[Hombre\], dark frame subtraction \[ffsup2, work in
progress\], TIFF ZIP compression \[Michal Thoma\], post-crop vignette
\[Wyatt Olson, work in progress\], luminance impulse denoising \[Emil
Martinec\], directional pyramid denoising \[Emil Martinec\], directional
pyramid equalizer \[Emil Martinec\], white balance tool will now
disregard clipped areas \[Emil Martinec\], and finally many areas have
been given multithreading support for faster execution on hardware that
supports it.

An overview of our top contributors and team members:

Gabor Horvath, aka Gabor (forum and googlecode). He lives in Budapest,
Hungary, and has enjoyed photography as a hobby since childhood. He
mostly uses a Nikon D90. He is the man who made all this possible. He
coded RawTherapee by himself right up to version 3.0-alpha1, which was
when he released the source code under a GPL license, on the 4th of
January 2010. Since then his main contribution has been the perspective
correction tool, a new curve editor, and refactoring the rtengine source
code (now called rtengine2.0) into a more maintainable and extensible
form which allows for things such as per-image demosaicing settings.
Once he is done with rtengine2.0, he plans on adding lensfun
integration, automatic chromatic aberration (purple fringe) removal and
implementing denoising before demosaicing. He would like to see
RawTherapee make use of GPU power for image processing algorithms in the
future using OpenCL.

Wyatt Olson, aka TheBigOne (forum) & wyatt.olson (googlecode). A Java
programmer by profession, he lives in Canda and has been shooting using
an Olympus DSLR since 2006 and film before that - mostly for fun, but
also for the occasional side dollar. His role in RT could be most
likened to a project admin - co-ordinating patches and answering
questions. He made the OSX standalone build scripts and compiles the
latest OSX builds. He is currently working on adding post-crop
vignetting. Wyatt wishes that the code was more modular and better
commented, and that there was a project leader to direct development. He
is happy to see that more people are contributing.

Emil Martinec, aka ejmartin (forum, googlecode) - check back soon\!

Ilya Popov, aka ilia (forum, googlecode). He currently lives in Den
Haag, Netherlands, and has been shooting as a hobby for 7 years mostly
on his Nikon D80 as of late. He is a developer and has contributed
mainly image resizing methods, a wavelet equalizer, histogram fixes and
keyboard shortcut additions. In the future, he plans on adding more
shortcut keys, a monochrome module with channel mixing, reworking
resizing algorithms, implementing an automatic generation of low
resolution images for internet use, and perhaps a command line
interface. He wishes that the RT code was refactored to simplify future
additions along with a transition to full floating point processing.

Hombre, aka Hombre54 (IRC), natureh (googlecode), Hombre (forum). He
lives in Vandoeuvre-les-Nancy in France. He has been a hobbyist film
photographer since 1993 using a Canon EOS 500N, but has been shooting
much more frequently since the digital revolution, using a Fuji Finepix
S9000, Pentax K10D and now a Pentax K20D. He wrote the initial
translation of the manual as well as the GUI into French, and then went
on to fix bugs, create the "control cage" curve editor, and code a class
which splits an image into small blocks that developers can use to take
advantage of parallelisation. He is currently devoting as much time as
he can to fixing bugs. He is planning to create a new "review" tab for
reviewing images, and to change the file browser so that embedded
thumbnails are loaded first in order to show a usable summary of a
directory as soon as possible, and only then to replace those embedded
thumbnails with generated ones using a fast demosaicing algorithm. He
would like to see RT integrating a local virtual gallery and a simple
web gallery, adding SVG signatures to photos, being able to switch from
the directory browser to a database driven file listing with tags.

David M. Gyurko, aka dualon (irc, forum). He lives in Budapest, Hungary,
and has been a hobbyist and semi-professional photographer since 2005,
shooting a few assignments per month using his Nikon D200. He is
responsible for forum management and acts as a middleman to Gabor. His
goal is to rethink and polish the GUI. He also plans to contribute
regular news updates from autumn onwards. He is learning C++ so that he
may contribute to the code in the future. He would like to see digital
asset management implemented in RawTherapee, as well as a batch rename
tool, browsing directories recursively as well as laterally, tagging,
fullscreen capabilities, fast image preview loading, black and white
processing tools and split/half/duotone effects.

Fabio Suprani, aka JOKER (forum) & ffsup2 (googlecode). He lives in
Italy and has enjoyed film photography as a hobby for a long time, only
recently having switched to digital using a Sony Alpha A200. He is a
developer and has fixed many bugs, as well as moved the progress bar to
the bottom, added a show/hide thumbnail information overlay button, a
few EXIF improvements, DCB optimization, and batch queue status changes.
He is currently working on an implementation of darkframe subtraction
from target photos, especially useful when long exposures are used. He
would like to see a new stable version of RT getting released as soon as
possible for fear of losing a portion of the userbase.

Paul Matthijsse, aka paul.matthijsse (forum), graveyron (IRC) - check
back soon\!

Andrey Skvortsov, aka Stingo (forum, googlecode) lives in Canada. He is
an advanced amateur, shooting often and for himself, currently using his
Olympus E-30. He has a clone of the RawTherapee source code where he
maintains the ribbon workflow, instead of the newer tabs one. He also
fixes bugs and helps implement OpenMP multithreading in the trunk. He
hopes to convince the community to the advantages of using a ribbon
workflow, as has been used in the past. He would also like a stable
version released as soon as possible.

Maciek Dworak, aka DrSlony (forum, IRC, googlecode). I currently live in
London, England. I made my first steps in developing black and white
film in 1998, and have been going slowly until I purchased my first
digital camera, a Fuji Finepix S5200, in 2005, which was when I realised
my passion for and character compatibility with photography. I have been
shooting virtual panoramas since 2006 and concerts since 2009. Like
David, I am only learning C++ and do not contribute code yet. I have
been a forum administrator since 2008 and offer usability and GUI
feedback and ideas. I lead the FaceBook RawTherapee group to help bring
the program out into the world, and write rawtherapee.com news articles,
this being the first major one. Seeing all the development since RT went
open does not leave much room for wishes. I am very impressed with the
work the brilliant people that joined us accomplished already, and hope
to see more talent join the team. I hope to see the future goals stated
above achieved, and wish that the soon to be formed steering committee
will be met with sanguinness and that it will be effective in
encouraging developers and assigning developer resources where they are
most needed, to please both the people behind the program, and the
users.

If you are not listed but feel you should, then please do forgive my
blunder and send me an email or private message in the forum. Check back
within 48 hours for added info on Emil Martinec and Paul Matthijsse
(sorry guys\!)

\- DrSlony

