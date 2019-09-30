# Carpentries@UGA hub page

[![Gem Version](https://badge.fury.io/rb/jekyll-theme-prologue.svg)](https://badge.fury.io/rb/jekyll-theme-prologue)

This is the web page for the Carpentries@UGA, to coordinate all Carpentries-related work at the Universitry of Georgia. The website theme is based on the [Prologue jekyll theme](https://chrisbobbe.github.io/jekyll-theme-prologue/) from [Chris Bobbe](https://chrisbobbe.github.io). This site is currently under development.

If you want to be involved in planning/running Carpentries workshops at UGA, please join the Carpentries@UGA conversation on Slack at https://join.slack.com/t/carpentriesuga/signup. (Note: If you use a @uga.edu email address, you should be able to join automatically.)

# Major site pages
HTML and markdown pages in the root directory become the major sections on the webpage. Index.html (or index.md) is the main landing page.

# Instructions/guide for where page components are

1. **Your `_config.yml` file must include the following line or your homepage won't work**: `collections: [sections]`. This tells Jekyll to look in the _sections folder (which you will create) for your content and render it all on one page.

2. **The `_sections` folder** in the root directory contains the major sections for the home page. Set a cover photo in any of the sections by adding `cover-photo: path/to/photo.jpg` and `cover-photo-alt: your alt text here` to the section's frontmatter. (Photos are currently stored in assets/images)

All new sections should be added as html or Markdown documents in the `_sections` folder. The following section variables can be set with [frontmatter](https://jekyllrb.com/docs/frontmatter/):
- `title` (required)
- `order` (required; orders the sequence of sections on the page. Example: `1`)
- `cover-photo` (optional; sets a background image for the section. Example: `assets/images/banner.jpg`)
- `cover-photo-alt` (required if using a cover photo. Describes the photo for screen readers and SEO; e.g. "Dome of Light art installation, Kaohsiung, Taiwan")
- `icon` (optional; see [Font Awesome](https://fontawesome.com/icons) for icon codes. Example: `fa-github`)
- `icon-style` (optional; "solid" is default, "regular" for outline style icons, or "brands" for logos)
- `auto-header` (optional; "use-title" is default, "none" for no header, or custom header text)
- `hide` (optional; if `true`, the section won't appear)

# Start blogging!

Jekyll has great resources to get you started writing blog posts. Check out [this Jekyll Docs page](https://jekyllrb.com/docs/posts/) first. When you've written a post or two, copy the following into a new file in your project directory called `blog.html`, and you'll see a link to your blog from the homepage:

```
---
layout: blog
title: My Blog
---
```

-- and that's it!

# Add a page

To add a page, just make a new .html or .md file in your project directory. There's an example called `reading-list` [provided](https://github.com/chrisbobbe/jekyll-theme-prologue/blob/master/reading-list.md) with the GitHub repository. Add this frontmatter:

```
---
title: My New Page
layout: page
---
```

You can also set these page variables in the frontmatter, if you want:
- `subtitle`
- `order` (orders links in the nav menu, e.g. `1`)
- `icon` (optional; see [Font Awesome](https://fontawesome.com/icons) for icon codes. Example: `fa-github`)
- `icon-style` (optional; "solid" is default, "regular" for outline style icons, or "brands" for logos)
- `hide` (optional; if `true`, a link won't appear in the nav menu. All this does is remove the nav link; your page will still be served to anyone who has the URL.)

**This same set of frontmatter variables (including `title`) can also be set in `index.md` and `blog.html`.** You may want to give them titles, or hide the homepage link with `hide: true` if the homepage is the only page.

For advanced SEO, this theme also lets you add `permalink` (see [Jekyll Docs](https://jekyllrb.com/docs/permalinks/#where-to-configure-permalinks)), `robots` (string, e.g. "noindex, nofollow"), and `canonical` (boolean; true is default) to any page or post.
