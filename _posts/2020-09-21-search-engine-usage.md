---
layout: post
title: Search engine usage with Google operators
description: Tips, hints and best practises for using Google & co.
date: 2020-09-21
author: Hardy Scheel
tags: [Google, SEO]
published: true
---

How does a search engine interpret your search queries? Your text queries are not interpreted like a prose text, which is very familiar for human understanding. Google for instance ignores stop-words like: and, for or the, and also interpunctuation. It picks out keywords, combines them and queries his databases for matches.

### Table of content
* [Google operators](#google-operators)
    * [Search operators](#search-operators)
        * [Further help](#further-help)
    * [Calculator](#calculator)
        * [Further help](#further-help)
    * [Colour Picker](#colour-picker)
        * [Further help](#further-help)
* [Google Operators in tabular form](#google-operators-in-tabular-form)
    * [Basic Google search operators](#basic-google-search-operators)
    * [Advanced Google search operators](#advanced-google-search-operators)

---

Google operators
================

## Search operators

`link:<domain>` - Which other websites have linked to this website? Example usage: Who has linked to your website or your blog entry?
```
link:scheel.dev
```

`site:<domain> your search queries` - Search the website you have specified.
```
site:scheel.dev java
java site:scheel.dev
```

`inurl:your search query` - Search a concrete part of the URL.
```
site:scheel.dev inurl:cmder
```

`info:<domain>` - Get site specific details and data. Get sites in google cache, similar sites or sites which are linked within this site.
```
info:scheel.dev
```

`define:your search query` - Get the definition about your query.
```
define:html
```

`cache:<domain>` - Get old cached versions of a site.
```
cache:scheel.dev
```

`related:<domain>` - Find similar sites.
```
cache:heise.de
```

### Further help

- [Google Search Help](https://support.google.com/websearch/answer/134479)
- [Google Search Help - optimize your search](https://support.google.com/websearch/answer/2466433)
- [German: online-marketing.de/google-suchoperatoren/](https://www.online-marketing.de/google-suchoperatoren/)
- [German: t3n.de/news/google-suche-tipps-und-tricks](https://t3n.de/news/google-suche-tipps-und-tricks-537407/)

## Calculator

You can calculate many things like:
- Arithmetic
- Functions
- Values of physical constants
- Conversion of number systems

Display equations graphically like:
- Trigonometric functions
- Exponential functions
- Logarithmic functions
- 3D graphics (for desktop browsers with WebGL support)

Geometry Calculator: Search for geometrical formulas and answers to complex geometrical problems.

Unit Converter:
- Temperature
- Unit of length
- Weight
- Speed
- Volume
- Area
- Fuel consumption
- Time
- Data size

### Further help

[Google Search Help - Use calculator, unit converter and colour picker](https://support.google.com/websearch/answer/3284611)

## Colour Picker

Use the colour picker to select a colour or convert one colour code to another.

### Further help

[Google Search Help - Use calculator, unit converter and colour picker](https://support.google.com/websearch/answer/3284611)


# Google Operators in tabular form

## Basic Google search operators


| Operator  | Purpose   | Example   |
| ------    |:-------:  | -------:  |
| +         | Search for several terms. Corresponds to the Google Standard Search. | Blog+Ratings |
| –         | Exclude terms. | Ice -Bear |
| \|        | The pipe symbol separates two terms and requires separate search results for both terms. | Bike+Helmet \| E-Bike |
| "…"       | Use quotation marks to search for a concrete sentence. | "The Kremlin in Moscow." |
| *         | Wildcard search. Search for unknown terms. | Airplane*Helicopter |
| .         | A dot automatically completes an omitted word in the search input. | The glorious. |
| ~         | Search for synonyms. | ~Evaluation |
| ..        | A from-to search. | iPhone 400..600$ |
| (...)     | Group operators and terms. | site:scheel.dev AND intitle:cmder |

## Advanced Google search operators

| Operator  | Purpose   | Example   |
| ------    |:-------:  | -------:  |
| allinanchor: | Suggests only search results that contain the desired search term in the link text. | allinanchor:designcapital |
| allinpostauthor: | Articles by a specific author can be found using the search command. | allinpostauthor:vargas llosa |
| allintext: | Only search results whose web page text contains all search terms will be displayed. | allintext:mostlivablecity |
| allintitle: | Only web pages are displayed whose titles contain all the search terms. | allintitle:urbangardening |
| allinurl: | Only returns search results from URLs that contain all desired search terms. | allinurl:designagency |
| AND | AND searches for results that meet all conditions of the search term. | site:Instagram.com AND site:facebook.com AND intext:flow magazin |
| AROUND (X) | AROUND offers results that are close to the search terms. The X expresses how many words may lie between the search terms. | AROUND(5) |
| cache: | Specifies the cache version of the searched website. | cache:amazon.com |
| define: | define offers the possibility to get definitions of the search term from various sources. | define:syntax |
| filetype: | Search results can be reduced to a specific file format, for example PDF. | recipe cheesecake filetype:pdf |
| inanchor: | Only websites whose text links contain desired search terms. | inanchor:colour theory |
| inauthor: | The author appears by name. | Inauthor:Jeff Bezos |
| info: | More information about the given page. | info:ebay.com |
| intext: | Searches only for text content that contains the search term. | intext:swim |
| intitle: | Searches only for title ads that contain the search term. | intitle:swim |
| inurl: | Only search results whose URL contains the specified search term. | inurl:illustrations |
| link: | Search only for content that links to the given URL. | link:amazon.com |
| OR | The OR parameter has the same function as the already mentioned pipe search operator and separates several search terms from each other; watch out for capitalization. | Geschäftsmodell OR Business Model Canvas |
| loc: | The search refers only to the specified location. | loc:Moscow |
| movie: | Cinema program regarding film and location are displayed. | movie:star wars |
| related: | Shows comparatively similar websites that you have specified. | related:news.com |
| site: | Search all pages of a domain indexed by Google. | site:www.news.com |
| weather: | Weather data refer to the location indicated. | weather:Moscow |