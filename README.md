# PaperModX

PaperModX is a forked version of [PaperMod](https://github.com/adityatelange/hugo-PaperMod),
it aims at adding new features and improving code quality,
makes it easier to read and modify by anyone with basic knowledge of Hugo and HTML.

Features and changes:
- Table of Contents (ToC) floating on the side
- InstantClick integration
- Social icons from [Simple Icons](https://simpleicons.org/)
- Opinionated UI enhancements

## Table of Contents (ToC) floating on the side

By adding config:

```yaml
params:
  TocSide: 'left'  # or 'right'
```

ToC will float on the left/right side of the page.
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

## Opinionated UI enhancements

- Distinguish home page width and post page width, post page is wider
  (800px) for better readability, you can change it by `--post-width` in `theme-vars.css`.
- Menu links are always bold, this feels more consistent when clicking around. Active links have deeper color.
