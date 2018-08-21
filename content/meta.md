---
title: "Meta"
date: 2018-08-16T13:11:37-05:00
draft: false
menu: "main"
weight: 10
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
- Add items to the main menu by adding the `menu: "main"` to the page's yaml metadata
- ~~Setup main menu to parse according to order in `data/Menu.toml`~~
    * ~~This is accomplished by setting the toml tags to a value:~~

            [01]
                ...

            [02]
                ...
      Check `data/Menu.toml` to see what I mean.

- Style the website (PIZZAZZ!)



[Hugo]: http://gohugo.io/
[Hyde-Y]: https://github.com/enten/hyde-y
