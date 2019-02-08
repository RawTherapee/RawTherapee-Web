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

The website is using the [Hugo][] static website generator.

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


Design Approach
---------------





[Hugo]: http://gohugo.io/
[Hyde-Y]: https://github.com/enten/hyde-y
