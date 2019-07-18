---
title: "Meta"
date: 2018-08-16T13:11:37-05:00
draft: false
menu: "main"
weight: 10
---

This is a meta file for the new rawtherapee.com website.

The repository is currently located at: https://gitlab.com/patdavid/rawtherapee-web.



Build
=====

The website is using the [Hugo][] static website generator with yarn (or npm if you must) to manage dependencies.

From the project root:

	cd themes/rt-hugo/assets
	yarn install

This should pull down the necessary dependencies, which consists of bootstrap 4 at the time of writing. It is important to use the `yarn` command in the `assets` directory, or else the SASS won't compile.

    $ hugo version
    Hugo Static Site Generator v0.54.0/extended

~~The base theme we are building off is called [Hyde-Y][].~~ We're building our own theme!

Calling `hugo` from the top of the project directory will cause Hugo to build the site into the `public/` folder.



Build + Serve
-------------

To build and serve the site while writing or testing you can (from the top of the project directory), call the Hugo comand:

    $ hugo server -D

Which will build the site and fire up a web server `http://localhost:1313`.
The `-D` option tells Hugo to build any draft files as well.


Content
-------

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
