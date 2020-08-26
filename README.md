# Website at scheel.dev
This is the source code of my website and the Jekyll theme at [scheel.dev](https://scheel.dev) hosted at GitHub Pages. Based on a Jekyll template [Cayman](https://github.com/pages-themes/cayman) which then got many extensions by me. Cayman is a Jekyll theme for GitHub Pages. You can [preview the theme to see what it looks like](http://pages-themes.github.io/cayman).

To run this blog at [scheel.dev](https://scheel.dev) the following things are involved:
- [*GitHub Pages*](https://pages.github.com/) as a webhost.
- [*Jekyll*](https://jekyllrb.com/) - A static website generator especially useful for blogs. Jekyll is served by GitHub Pages.
- [YAML](https://yaml.org/) - YAML data serialization language is build in the template to make fast configurations all across the web site.

## Table of contents
- [Jekyll's role as a static site generator](#jekyll's-role-as-a-static-site-generator)
- [Template layout](#template-layout)
    - [Available YAML Front Matter variables](#available-yaml-front-matter-variables)
- [Prose.io as web based content authoring editor](#prose-as-web-based-content-authoring-editor)
- [Stylesheet](#Stylesheet)
- [Layouts](#Layouts)

---

## Jekyll's role as a static site generator
Static site generator means that the pages are built just once and just being served when their URL is hit, rather than being dynamically created with every page load.

## Template layout
This is a reusable template to use it for other projects, its components are generalized and reusable as possible. A good starting point to learn to how to build components.

### Available YAML FRONT MATTER variables

```YAML
---
layout: default | post
title:	Your big heading on the specific page or post. Acts as a main title. If no title is used the default title in _config.yml is used.
description: Your site or blog description that acts as a title. If no description is used the default description in _config.yml is used.
date: When was your blog post created. If no date exists the file name is used. (optional)
last_update: When did up update your existing blog post. (optional)
author: Who has written this blog post.
tags: [java, html] Add tags of your choice. To categorize blog posts. (optional)
lang: The language of the current page. Default language is 'en' set in _config.yml.
published: true | false Set to false if you don’t want a specific post to show up when the site is generated.

-- Jekyll optional vars
date: overrides the date from the file name YYYY-MM-DD HH:MM:SS
permalink: (default /blog/title)
---
```
## Prose as web based content authoring editor
In combination with [Prose.io](https://prose.io/#about), a web based content authoring environment, you can use Prose as a MarkDown editor to add and edit blog posts very quickly. To use it on your own you have to give Prose.io access to your GitHub account if the source code of your Jekyll blog is hosted at GitHub Pages.

## Stylesheet
If you'd like to add your own custom styles:

1. Create a file called `/assets/css/style.scss` in your site
2. Add the following content to the top of the file, exactly as shown:
    ```scss
    ---
    ---

    @import "{{ site.theme }}";
    ```
3. Add any custom CSS (or Sass, including imports) you'd like immediately after the `@import` line

*Note: If you'd like to change the theme's Sass variables, you must set new values before the `@import` line in your stylesheet.*

## Layouts
If you'd like to change the theme's HTML layout:

1. [Copy the original template](https://github.com/pages-themes/cayman/blob/master/_layouts/default.html) from the theme's repository<br />(*Pro-tip: click "raw" to make copying easier*)
2. Create a file called `/_layouts/default.html` in your site
3. Paste the default layout content copied in the first step
4. Customize the layout as you'd like