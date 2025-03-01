---
layout: post
title: Markdown resource collection
description: A collection of tutorials and links for Markdown markup language.
date: 2018-12-29
last_update: 2020-09-21
author: Hardy Scheel
tags: [Markdown, CommonMark]
---

<!--
Markdown resource collection
A collection of tutorials, tools and links to get to know Markdown as a markup language.
A collection of tutorials and links for Markdown markup language.
-->

Markdown
========

Markdown is a simple way to write, structure and format text. And all at the same time when you write the text.

## Tutorials
- [German: Markdown: Anleitung für die einfache Auszeichnungssprache](https://www.ionos.de/digitalguide/websites/web-entwicklung/markdown/)
- [German: Einführung, Syntax und Beispiele inkl. GitHub Flavoured Markdown](http://markdown-syntax.de/Syntax/)
- [interactive Markdown tutorial @markdowntutorial.com](http://markdowntutorial.com/)
- [interactive Markdown tutorial @commonmark.org](https://commonmark.org/help/tutorial/)

## Cheat Sheets
- [Markdown syntax cheat sheet @github.com/adam-p](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
- [Markdown reference quick overview @commonmark.org](https://commonmark.org/help/)
- [Markdown quick guide @github.com](https://guides.github.com/features/mastering-markdown/)

## Editors
- [StackEdit – in-browser Markdown editor](https://stackedit.io/)

## Syntax highlighting in code blocks

Code blocks are part of the MarkDown specification but syntax highlighting is not. But many renderers like GitHub support syntax highlighting. Just open a code block and define your language or shell you want to colour.

- Look what languages are supported by syntax highlighting: [https://highlightjs.org/static/demo/](https://highlightjs.org/static/demo/)

Example usage:
```javascript
    ```javascript
    for (var i = 0 / 2; i < classes.length; i++) {
        if (checkCondition(classes[i]) === undefined)
        console.log('undefined');
    }
    ```
```

## LaTeX/Mathematics / TeX Mathematical Formulae

Some renderers can interpret LaTeX Mathematics. The beginning and ending dollar signs (`$`) are the delimiters for the TeX markup.

- [https://en.wikibooks.org/wiki/LaTeX/Mathematics](https://en.wikibooks.org/wiki/LaTeX/Mathematics)

Examples:
```latex
$-b \pm \sqrt{b^2 - 4ac} \over 2a$
$x = a_0 + \frac{1}{a_1 + \frac{1}{a_2 + \frac{1}{a_3 + a_4}}}$
$\forall x \in X, \quad \exists y \leq \epsilon$
```


CommonMark
==========

CommonMark is a propose for an unambiguous syntax reference specification for Markdown.
- [CommonMark website](https://commonmark.org)
- [CommonMark specification](https://spec.commonmark.org/)
- [GitHub Flavored Markdown Spec - based on CommonMark](https://github.github.com/gfm/)