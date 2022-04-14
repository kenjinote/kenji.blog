---
title: "PaperModX New Features"
date: 2022-04-12T23:37:00+08:00
weight: 1
---


This page explains the new features and changes of PaperModX
comparing to it's origin PaperMod.


## Table of Contents (ToC) floating on the side

By adding config:

```yaml
params:
  TocSide: 'left'  # or 'right'
```

ToC will float on the left/right side of the page.
You can take a look at how `'right'` feels like in [Installation | Update](../papermod/papermod-installation).

The ToC box is responsive, it only shows on the side when minimum screen size is 1440px.

this feature is enabled on this site.


## InstantClick integration

By adding config:

```yaml
params:
  EnableInstantClick: true
```

[InstantClick](http://instantclick.io/) will be enabled,
making navigation behaves like Single Page Application.

Note that `/search` pages are omitted from InstantClick
to prevent conflicts from search's JavaScript,
this may be changed in the future after refactoring those scripts.

Another thing to notice is smooth scrolling will be disabled
if InstantClick is enabled, because they both listen click
event on every `<a>` tags. IMO smooth scrolling is not very useful
so it has to give way to InstantCllick.

This feature is enabled on this site.


## Social icons from Simple Icons

Add social icons with `-simple` suffix from [Simple Icons](https://simpleicons.org/).

Available icons:
- github-simple
- rss-simple
- telegram-simple
- twitter-simple
- pinboard-simple

The icons are moved from `layouts/partials/svg.html` to `data/svg.toml`,
makes it easier to maintain, it's now possible to have an index page
to show all the icons, check it out at: [Icons Preview](../../icons)

## Opinionated UI enhancements

- Distinguish home page width and post page width, post page is wider
  (800px) for better readability, you can change it by `--post-width` in `theme-vars.css`.
- Menu links are always bold, this feels more consistent when clicking around. Active links have deeper color.
