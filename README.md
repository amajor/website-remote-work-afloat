# README

## Remote Work Afloat Website

### Start Dev Server

```bash
bundle exec jekyll serve
```

For help, go to https://jekyllrb.com/docs

## Site Organization

### Front Matter

#### Articles

Articles are written in markdown (.md) files. The articles should contain front 
matter to fill in the templates. 

At minimum, every page must have the front matter lines to render the 
liquid elements:

```yml
---
---
```

Normal posts will be more filled out:

```yml
---
title: "Best Boat Router for Loopers"
date: 2025-12-05 08:00:00 -0500
category: Remote Work
tags:
  - digital-nomad
  - internet-connections
  - work-from-anywhere
permalink: /articles/boat-connectivity-101
article_title: Boat Connectivity 101
article_excerpt: This excerpt will show on the home page with links to posts.
---
```

| **PROPERTY**      | **NOTE**                                                                                                                                 |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| `title`           | SEO title.<br>This title will be used for SEO and in the browser tab.<br>It's a fallback title if the `article_title` is not filled out. |
| `excerpt`         | SEO description.                                                                                                                         |
| `date`            | The publish date of the article. Format:<br>`2025-12-05 08:00:00 -0500`                                                                  |
| `category`        | The article category.                                                                                                                    |
| `tags`            | The organizational tags for an article                                                                                                   |
| `permalink`       | The relative path for an article                                                                                                         |
| `article_title`   | Used in the article page when present.<br>It falls back to `title` if this isn't present.                                                |
| `article_excerpt` | Used when we need a small excerpt.                                                                                                       |

#### Testimonies

Testimonies are managed in `_data/testimonies.yml`.

The following format can be used for each testimony:
```yml
- name: Billy Bob
  testimony: "“This was a great book”"
  rating: 5
  link: https://amazon-review-link
```

### External Articles

#### Loop Life Academy

Articles that are from Loop Life Academy can be added as post by creating files
in the folder `_posts/looplifeacademy` and giving it appropriate front matter.

The primary difference is that we're adding an `external` property that will
contain the link to looplifeacademy.com. The templates will automatically link
to the site instead of to the internal page, so the content of the file may
be left blank.

```md
---
title: "Staying in Touch While Cruising: Tools for Email, Messaging & More"
date: 2025-08-18 08:00:00 -0500
category: Remote Work
tags:
  - loop-life-academy
  - internet-connections
  - work-from-anywhere
permalink: /articles/looplifeacademy/staying-in-touch-while-cruising-tools-for-email-messaging-more
external: https://www.looplifeacademy.com/blog/staying-in-touch-while-cruising-tools-for-email-messaging-more
article_title: "Staying in Touch While Cruising: Tools for Email, Messaging & More"
article_excerpt: Cruising doesn’t mean going off the grid entirely. Here’s how our family stays connected with email, messaging apps, video calls, and offline tools—whether we’re at anchor, underway, or out of cell range.
---
````

### Gear

The front matter for gear includes a number that references the order the
categories fall in `_data/gear.yml`:

```yml
---
layout: page_gear_items
title: Necessary Devices
permalink: /gear/necessary-devices
category: 0
---
```

## Styling & Plugins

### Theme: Minima

The default theme for Jekyll is _minima_.

To customize, we can grab a few baseline files from their repo to overright.

Check out the files here: https://github.com/jekyll/minima/tree/master

### Plugin: Jekyll Sitemap
jekyll-sitemap - Creates a sitemap file to help search engines index content

TODO: Install and use this plugin

### Plugin: Jekyll Feed
jekyll-feed - Creates an RSS feed for your posts

TODO: Install and use this plugin

### Plugin: Jekyll SEO Tag
jekyll-seo-tag - Adds meta tags to help with SEO

TODO: Install and use this plugin that was part of the minima theme.

https://github.com/jekyll/jekyll-seo-tag/tree/master