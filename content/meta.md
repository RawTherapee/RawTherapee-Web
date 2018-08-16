---
title: "Meta"
date: 2018-08-16T13:11:37-05:00
draft: false
---

This is a meta file for the new rawtherapee.com website.

Build
-----

The website is using the [Hugo][] static website generator.

    $ hugo version
    Hugo Static Site Generator v0.46

The base theme we are building off is called [Hyde-Y][].

Calling `hugo` from the top of the project directory will cause Hugo to build the site into the `public/` folder.

### Build + Serve

To build and serve the site while writing or testing you can (from the top of the project directory), call the Hugo comand:

    $ hugo server -D

Which will build the site and fire up a web server `http://localhost:1313`.  
The `-D` option tells Hugo to build any draft files as well.


Todo
----

- Remove pages from being parsed in RSS feed.
- Style the website (PIZZAZZ!)



[Hugo]: http://gohugo.io/
[Hyde-Y]: https://github.com/enten/hyde-y
