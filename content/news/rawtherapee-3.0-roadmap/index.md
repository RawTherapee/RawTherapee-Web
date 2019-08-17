---
title: "RawTherapee 3.0 Roadmap"
date: 2010-11-24T09:39:00+00:00
author: dualon
Tags:
- Future Plans
- RT 3.0
---



From now every major release will have a roadmap. Each will be named
after the current release, they detail the current trends and draft the
future plans. Please note that roadmaps are not laws carved in stone:
these are indeed plans which may change with time.

The current one for the 3.0 branch can be found
below: this is how RT OSMC (in
alphabetical
order: DrSlony, dualon, ejmartin, Gabor, Hombre, janrinze,
paul.matthijsse, TheBigOne) envisions the next few weeks. The discussion
of the roadmap [can be found here](../forum/viewtopic.php?t=2404).  

Please keep in mind that the plans outline an extremely fast
progression. That is because we really want to have a stable release as
soon as possible and it is beleived that it may be achieved, but the
more realistic is that it will be ready only in the next year.  
If we reach the beta phase for the holidays that would be already a
great achievement.

Short-term roadmap  
  
1\. Announce feature freeze  
Feature freeze will be announced on the website. Only bugfixes and GUI
enhancements will be accepted for a short period. The new features will
be included in the continued development tree shortly after the feature
freeze, see below.  
24th November.  
  
2\. Clean-up RT  
Find the deprecated elements and redundancies in RT algorythms, GUI
elements, etc. and remove them.  
28th November.  
  
3\. Discuss the pp3 format  
The pp3 files should save all the current settings and should be
future-proof (as much as they can be). Partial profile application (lets
say a pp3 includes only WB data) should be enabled too.  
The less the conversion of sidecar files are, the better it is for users
as well as for devs, so a thorough planning would be advisable.  
28th November, parallel with clean-up.  
  
4\. Branch the repository  
The main branch will remain the "development branch" and
~~it will be renamed to "rawtherapee-head", or "head"~~
it will remain called "default". A
new "3.0\_branch" will be introduced. Every bleeding edge development
can go into the "head", the 3.0 will accept only bugfixes and GUI
enhancements. The commits of the 3.0 branch may be reintroduced to the
head at a point later, most probably in big bunches.  
28th November, or as soon as the clean-up is finished.  
  
5\. Implement pp3 changes.  
10-13th December.  
  
6\. Fix known critical bugs, release RawTherapee 3.0 beta-1.  
The beta-1 should feature all the algorythms and GUI elements as they
will be released in the final version. All, or at least all the critical
bugs should be fixed in this version (although it may contain some known
bugs).  
20th December.  
  
7\. Release beta-2/RC  
If and when needed. Hopefully we can jump this step.  
  
8\. Release RawTherapee 3.0 stable.  
If we are lucky it can be out until Christmas, but the more realistic is
that we can announce it between X-mas and New Year or in the New Year.
It would be great to let the users use a stable, or at least
almost-stable version during the holidays.  
Happy-happy RawTherapee community\! :)  
  
9\. Maintanance of 3.0.x branch  
The 3.0.x branch will be maintained with dcraw updates and maybe
bugfixes until the next RC/stable release of RT.  
  
  
**Mid-term plans**
  
\- rtengine2  
\- Color tools in Lab colorspace  
\- updating documentation  
\- new profiles for portraits, landscapes, B\&W shots, etc.  
  
  
**Mid- and/or long-term roadmap**
  
\- plugin system in RT based on rtengine2?  
\- CustomProfileBuilder v2 (as a plugin?)  
\- GUI redesign: modular (plugin-based) GUI (maybe based on the QT
framework?)  
\- revision of color management in RT  
\- adding more digital asset management features (tagging of images,
maybe showing all the images from different folders in Thumbnail
Browser)  
\- Black & White tools: testing the current features, adding more if
needed  
\- HDR tools

---

dualon  


