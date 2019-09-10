[![pipeline status](https://gitlab.com/patdavid/rawtherapee-web/badges/master/pipeline.svg)](https://gitlab.com/patdavid/rawtherapee-web/commits/master)

# The RawTherapee.com website

This is the repository for the new RawTherapee.com website.

## Hugo

We're currently using:

```
Hugo Static Site Generator v0.58.1/extended
```

Note that you'll need the extended version of Hugo (https://github.com/gohugoio/hugo/releases).

We are using Hugo as built by @darix (https://build.opensuse.org/package/show/home:darix:apps/hugo).

To build the site locally once it's been cloned needs two steps:

1. `cd` into `/themes/rt-hugo/assets/` and run `yarn install` (or `npm install`).
2. Back at the project root, run the Hugo server `$ hugo server -D --disableFastRender`.

This will provide the site locally at `http://localhost:1313`.
It will also monitor the directories and re-build on any changes (and reload the page).o

For further details on writing and publishing content see `/about/meta/`.

## GitLab Pages

GitLab runs a CI service that builds all commits against the master branch, and publishes them here: https://patdavid.gitlab.io/rawtherapee-web/.

The CI/CD build now also publishes the site to the webhost on any merges/pushes to the `master` branch.


## Netlify

**This is still experimental right now.**
We've also integrated [Netlify][] into the site as a CMS/post-editor while still mainting a GitLab based back-end.
If you have push permissions on the repo, you can access the editor at `/admin` (so while we're testing here on gitlab pages, it would be: https://patdavid.gitlab.io/rawtherapee-web/admin

[Netlify]: https://www.netlify.com/


## Front Page Carousel of Images

To add/remove images from the sliding carousel of screenshots on the front page simply add or remove images frmo the directory `/static/images/carousel`.  The template will parse all the images in this directory and automatically add them to the carousel.
