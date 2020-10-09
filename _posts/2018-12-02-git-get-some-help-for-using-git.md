---
layout: post
title: Get some help for using git
description: A collection of resources for getting started for git and for solving problems with git.
date: 2018-12-02
last_update: 2020-10-09
author: Hardy Scheel
tags: [git, GitHub]
published: true
---

<!--
Get some help for using git
A collection of resources for getting started for git and for solving problems with git.
-->

### Table of content
- [Useful CLI Commands](#useful-cli-commands)
- [Tutorials](#tutorials)
- [Cheat Sheets](#cheat-sheets)
- [Solving Problems](#solving-problems)
- [Helpful Tools](#helpful-tools)
- [FAQ](#faq)
    - [Change the user for a repository](#change-the-user-for-a-repository)

----

## Useful CLI Commands

**Viewing Commit History**
```shell
git log --all --decorate --oneline --graph
```

----

## Tutorials
Get to know git as a version control system.
- [Pro Git e-book in various languages](http://git-scm.com/book){:target="_blank"}
- [Official Git introduction tutorial](https://git-scm.com/docs/gittutorial){:target="_blank"}
- [A guided tour through Git fundamentals](http://gitimmersion.com){:target="_blank"}
- [Git for GitHub handbook](https://guides.github.com/introduction/git-handbook/){:target="_blank"}

---

## Cheat Sheets 
Get a quick overview of relevant git commands for your daily work.
- [GitHub's Git CLI Cheat Sheets - overview](https://services.github.com/on-demand/resources/cheatsheets/){:target="_blank"}
- [GitHub's Git CLI Cheat Sheets](https://services.github.com/on-demand/downloads/github-git-cheat-sheet/){:target="_blank"}
- [GitHub's Git CLI Cheat Sheets - as a PDF](https://services.github.com/on-demand/downloads/github-git-cheat-sheet.pdf){:target="_blank"}
- [GitHub's Git CLI Cheat Sheets - German](https://services.github.com/on-demand/downloads/de/github-git-cheat-sheet/){:target="_blank"}

---

## Advanced Git usage

- [GitHub Cheat Sheet](https://github.com/tiimgreen/github-cheat-sheet) - Powerful tips and use cases
- [A Visual Git Reference](https://marklodato.github.io/visual-git-guide/index-en.html) - Graphical in-depth Git knowledge
- [A Visual Git Reference - German](https://marklodato.github.io/visual-git-guide/index-de.html)
- [Visualizing Git Concepts with D3](https://onlywei.github.io/explain-git-with-d3)

---

## Solving Problems
- [Setting up multiple GitHub accounts on Windows](http://www.kevinpelgrims.com/blog/2012/07/20/setting-up-multiple-github-accounts-on-windows/){:target="_blank"}

---

## Helpful Tools

* [Git Kraken GUI](https://www.gitkraken.com) \- Best graphical tool for managing commits & merge conflicts
* [Sublime Merge](https://www.sublimemerge.com) \- Very good graphical git merge tool

----

## FAQ

### Change the user for a repository
Git uses a hierarchical configuration of multiple levels. Settings in higher levels override values in lower levels. Lower levels inherit from higher levels (eg. *local* inherits from *global*).
- **system** - Settings for all users of the system are stored in git installation folder: `your-git-installation-folder/etc/gitconfig`
- **global** - Settings for the current user are stored locally in your user home directory: `~/.gitconfig`
- **local** - The current repository settings are stored locally in the repository directory: `.git/config`

You can configure an individual repository to use a specific user which overrides the *global* configuration. From the root directory of the repository, run the following on command line:

~~~shell
$ git config user.name "your name"
$ git config user.email your@email.com
~~~

The default user for all repositories is configured in the *global* configuration file in your home directory `~/.gitconfig`. You can also run the following from command line:

~~~shell
$ git config --global user.name "your name"
$ git config --global user.email your@email.com
~~~
