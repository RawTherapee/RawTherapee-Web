[![pipeline status](https://gitlab.com/patdavid/rawtherapee-web/badges/master/pipeline.svg)](https://gitlab.com/patdavid/rawtherapee-web/commits/master)

# The RawTherapee.com website

This is the repository for the new RawTherapee.com website.

## Hugo

Note: As of this writing (2018-08-22), Hugo from the repos on Ubuntu 18.04 is a little outdated and doesn't included the "extended" Sass/SCSS version (0.47.1).
On these systems, better to use the snap:

    sudo snap install hugo


## GitLab Pages

GitLab runs a CI service that builds all commits against the master branch, and publishes them here: http://patdavid.gitlab.io/rawtherapee-web/.


## Netlify

We've also integrated [Netlify][] into the site as a CMS/post-editor while still mainting a GitLab based back-end.
If you have push permissions on the repo, you can access the editor at `/admin` (so while we're testing here on gitlab pages, it would be: http://patdavid.gitlab.io/rawtherapee-web/admin


[Netlify]: https://www.netlify.com/
