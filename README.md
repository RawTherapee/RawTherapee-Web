[![pipeline status](https://gitlab.com/patdavid/rawtherapee-web/badges/master/pipeline.svg)](https://gitlab.com/patdavid/rawtherapee-web/commits/master)

# The RawTherapee.com website

This is the repository for the new RawTherapee.com website.

## Hugo

~~Note: As of this writing (2018-08-22), Hugo from the repos on Ubuntu 18.04 is a little outdated and doesn't included the "extended" Sass/SCSS version (0.47.1).
On these systems, better to use the snap:~~

    ~~sudo snap install hugo~~

We are using Hugo as built by @darix (https://build.opensuse.org/package/show/home:darix:apps/hugo).

To build the site locally once it's been cloned needs two steps:

1. `cd` into `/themes/rt-hugo/assets/` and run `yarn install` (or `npm install`).
2. Back at the project root, run the Hugo server `$ hugo server -D --disableFastRender`.

## GitLab Pages

GitLab runs a CI service that builds all commits against the master branch, and publishes them here: https://patdavid.gitlab.io/rawtherapee-web/.


## Netlify

**This is still experimental right now.**
We've also integrated [Netlify][] into the site as a CMS/post-editor while still mainting a GitLab based back-end.
If you have push permissions on the repo, you can access the editor at `/admin` (so while we're testing here on gitlab pages, it would be: https://patdavid.gitlab.io/rawtherapee-web/admin

[Netlify]: https://www.netlify.com/


## Front Page Carousel of Images

To add/remove images from the sliding carousel of screenshots on the front page simply add or remove images frmo the directory `/static/images/carousel`.  The template will parse all the images in this directory and automatically add them to the carousel.
