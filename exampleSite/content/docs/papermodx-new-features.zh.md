---
title: "PaperModX 新功能说明"
date: 2022-04-12T23:37:00+08:00
summary: 本文档描述 PaperModX 相比原版 PaperMod 增加的新功能和变化。
weight: 1
---


本文档描述 PaperModX 相比原版 PaperMod 增加的新功能和变化。


## Table of Contents (ToC) floating on the side

By adding config:

```yaml
params:
  TocSide: 'left'  # or 'right'
```

ToC will float on the left/right side of the page.
You can take a look at how `'right'` feels like in [Installation | Update](https://reorx.github.io/hugo-PaperModX/docs/installation/).

The ToC box is responsive, it only shows on the side when minimum screen size is 1440px.

This feature is enabled on this site.


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


## Give links an accent color.

Though PaperModX is designed to be minimal, accent color is still essential.
It's a good way to show personality and make your site feels more delightful.

The default color is a purple vibe,
you can customize the colors of link, link underline and their hover variants
by override the following css variables in `assets/css/extended/custom.css` of your site.

```css
:root {
  --link-color: var(--primary);
  --link-hover-color: #573eaa;
  --link-underline-shadow: 0 1px 0 var(--link-color);
  --link-hover-underline-color: #573eaa;
  --link-hover-underline-shadow: 0 2px 0 var(--link-hover-underline-color);
}
```


## Customize pagniator size

In section pages, if you want the paginator size be different from the
[global config](https://gohugo.io/templates/pagination/#configure-pagination),
you can add `paginate` in the frontmatter to customize.

```yaml
---
paginate: 10
---
```


## Menus external link

You can add `external: true` to a menu item's params to mark it as an external link,
this will add a small icon to the end, and make the link open in new tab when clicked.

```yaml
menu:
  main:
    - name: "@Author"
      url: "https://reorx.com"
      params:
        external: true
```


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
to show all the icons, check it out at: [Icons Preview](https://reorx.github.io/hugo-PaperModX/docs/icons_preview/)


## Opinionated UI enhancements

- Distinguish home page width and post page width, post page is wider
  (800px) for better readability, you can change it by `--post-width` in `theme-vars.css`.
- Menu links are always bold, this feels more consistent when clicking around. Active links have deeper color.
