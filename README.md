This is the source code of my website and the Jekyll theme at [scheel.dev](https://scheel.dev) hosted at GitHub Pages. Based on a Jekyll template [Cayman](https://github.com/pages-themes/cayman) which then got many extensions by me. Cayman is a Jekyll theme for GitHub Pages. You can [preview the theme to see what it looks like](http://pages-themes.github.io/cayman).

To run this blog at [scheel.dev](https://scheel.dev) the following things are involved:
- [*GitHub Pages*](https://pages.github.com/) as a webhost.
- [*Jekyll*](https://jekyllrb.com/) - A static website generator especially useful for blogs. Jekyll is served by GitHub Pages.
- [YAML](https://yaml.org/) - YAML data serialization language is build in the template to make fast configurations all across the web site.

### Table of contents
- [Jekylls role as a static site generator](#jekylls-role-as-a-static-site-generator)
- [Template layout](#template-layout)
    - [Available YAML Front Matter variables](#available-yaml-front-matter-variables)
- [Prose.io as web based content authoring editor](###prose-as-web-based-content-authoring-editor)

---

## Jekylls role as a static site generator
Static site generator means that the pages are built just once and just being served when their URL is hit, rather than being dynamically created with every page load.

## Template layout
This is a reusable template to use it for other projects, its components are generalized and reusable as possible. A good starting point to learn to how to build components.

### Available YAML FRONT MATTER variables

```YAML
---
layout: default | post
title:	Your big heading on the specific page or post.
description: Your site or blog description that acts as a title.
tags: [java, html] Add tags of your choice.

-- Jekyll optional vars
date: overrides the date from the file name YYYY-MM-DD HH:MM:SS
permalink: (default /year/month/day/title.html)
---
```
## Prose as web based content authoring editor
In combination with [Prose.io](https://prose.io/#about), a web based content authoring environment, you can use Prose as a MarkDown editor to add and edit blog posts very quickly. To use it on your own you have to give Prose.io access to your GitHub account if the source code of your Jekyll blog is hosted at GitHub Pages.