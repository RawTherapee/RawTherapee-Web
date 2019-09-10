---
title: "Meta"
date: 2018-08-16T13:11:37-05:00
draft: false
weight: 10
---

This is a meta file for the new rawtherapee.com website.
It will cover some basics for using the Hugo Static Site Generator and where content should go and be added.

The repository is located at: https://gitlab.com/patdavid/rawtherapee-web.



## Build

The website is using the [Hugo][] static website generator with yarn (or npm if you must) to manage dependencies.

If you don't have it installed yet, you may need to install `yarn` with:
```
npm -g install yarn
```

From the project root:

	cd themes/rt-hugo/assets
	yarn install

This should pull down the necessary dependencies, which consists of bootstrap 4 at the time of writing.   
_It is important to use the `yarn` command in the `assets` directory, or else the SASS won't compile._

    $ hugo version
    Hugo Static Site Generator v0.54.0/extended


Calling `hugo` from the top of the project directory will cause Hugo to build the site into the `public/` folder.


### Build + Serve

To build and serve the site while writing or testing you can (from the top of the project directory), call the Hugo comand:

    $ hugo server -D --disableFastRender

Which will build the site and fire up a web server at `http://localhost:1313`.  
The `-D` option tells Hugo to build any draft files as well.

This will monitor the project directories for any changes and rebuild if it detects them.
It will also auto-reload the page for you.


## Content

There are two main areas for creating content: `news` and `downloads`.


### News

`news` items are envisioned to be similar to blog posts - informational and general project posts.

To create a new post, create a directory under `/content/news/`.  
We recommend using a format like: `YYYY-MM-DD-post-title`. (It makes directory listing and finding posts a little easier.)

Inside that directory, create an `index.md` file and any assets you may want to reference (images, etc).  
This makes it easy to package a post up in a single directory with all relevant assets.

For example:

```
.
└─ content
   └── 2019-09-09-new-rawtherapee-website
       ├── index.md
       └── new-screenshot.jpg
```

The `index.md` file is a [Markdown file][] that will need some basic frontmatter at the top for metadata:

[Markdown file]: https://gohugo.io/content-management/formats/#learn-markdown

```
---
title: "Support Freedom, Donate a Kidney!"
date: 2017-11-23T15:47:00+00:00
author: DrSlony
---

You can help not only RawTherapee, but the open-source photographic
community as a whole, and it won't cost you a dime nor a kidney. You
don't even need to know how to code. Here's how.
<figure>
<a href="new-screenshot.jpg"><img src="new-screenshot.jpg" alt=""></a>
</figure>
```

The posts should have at least `title`, `date`, and `author`.  
The date should be in [ISO 8601][] format, with at least `YYYY-MM-DD`.  
(A full datetime stamp is better as it avoids trying to build pages in the future if someone else pulls the repo in a different timezone.)

[ISO 8601]: https://en.wikipedia.org/wiki/ISO_8601

Yes, you can use valid HTML in Markdown files - in this case I prefer to use the `<figure>` tag for images for example.  


### Downloads

The `downloads` content type is intended for release posts.

To create a new `downloads` post, create a new directory under `/content/downloads/`.  
A good practice is to use a name like `5.7.md` or `5.7-RC1`.
It's up to you how you name it, but the slug will reflect the directory name here, so something like this:
```
.
└─ content
   └── downloads
       └── 5.7-RC1
           ├── index.md
           └── new-screenshot.jpg
```
would have a url like `https://www.rawtherapee.com/downloads/5.7-RC1/`.

The frontmatter will look similar, but needs a few extra things.

```
---
title: "RawTherapee version 5.6"
date: 2019-04-20T22:22:12+02:00
draft: false
version: "5.6"
linux_binary: "https://rawtherapee.com/releases_head/linux/RawTherapee-releases-5.6-20190420.AppImage"
windows_binary: "https://rawtherapee.com/releases_head/windows/RawTherapee_5.6_WinVista_64.zip"
mac_binary: "https://rawtherapee.com/releases_head/mac/RawTherapee_OSX_10.9_64_5.6.zip"
source_code: "http://rawtherapee.com/shared/source/"
---
```
Besides the usual `title` and `date` (and `draft` if you need it) are some new metadata properties to help build the correct links:

* `version` for the version number
* `(linux|windows|mac)_binary` for each platform binary link
* `source_code` for the tarballs

Hugo will build the links for each binary automatically and update the version numbers and dates for the download buttons on the top of each page as well as the most recent version on the top of the homepage.

---

#### Notes

The directory structure will change how the site builds out and which layouts get used.
Pat prefers to be able to mimic directory structure on-disk as page navigation (excepting blog posts).

So pages might look like this:

```
.
└─ content
   ├── about.md
   ├── features.md
   └── meta
       ├── _index.md
       └── design.md
```

The use of an `_index.md` file under a directoy triggers Hugo to treat it as a "section".
This also means that it uses the section template/layout (defaulting to `{theme}/layouts/_default/section.html`.

If you don't want to hack at the `section.html` layout, then you can explicitly set the layout in the yaml of a page file `layout: single` for instance (this would use the `single.html` layout from the same location listed above).


Design Approach
---------------





[Hugo]: http://gohugo.io/
[Hyde-Y]: https://github.com/enten/hyde-y
