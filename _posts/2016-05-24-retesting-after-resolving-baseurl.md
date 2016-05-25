---
layout: post
title:  "Retesting after Resolving Baseurl"
date:   2016-05-24 19:42:14
categories: jekyll update
---

Had considerable issues getting the site to render correctly in GitHub Pages. After much hunting around, discovered the issue was with the `baseurl` option in the `_config.yml` file. It needed to be set to the name of my project repository I'm using for the site (`test-jekyll-site`):

```yaml
# Site settings
title: Test Jekyll Site
email: your-email@domain.com
description: > # this means to ignore newlines until "baseurl:"
  Just a test site to use as a sandbox and play around with learning Jekyll.
baseurl: "/test-jekyll-site" # the subpath of your site, e.g. /blog
```

This wasn't very clear from the description "the subpath of your site."

Also, once I fixed this so the GitHub Pages site worked, the local version for testing (on localhost) quit working. Had to also tack `/test-jekyll-site/` onto the end of the localhost URL.

Thankfully found useful information here: [Clearing Up Confusion Around baseurl – Again - By Parker](https://byparker.com/blog/2014/clearing-up-confusion-around-baseurl/).