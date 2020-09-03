---
layout: post
title: Setting up Cmder with Git
description: Use your already existing Git for Windows with Cmder-mini.
date: 2020-09-01
author: Hardy Scheel
tags: [git, cmder]
published: true
---

<!--
Setting up Cmder with Git
Use your already existing Git for Windows with Cmder-mini.
-->

----

We are setting up Cmder-mini (currently at version 2.8.0) with an already installed Git for Windows bash to use git bash within Cmder-mini. Cmder-mini does not include Git and is a way more lightweight than the full Cmder variant. When combining them you benefit from your already made and existing setting in Git for Windows.

To start the the Cmder configuration open Cmder and press "Win + Alt + T" keys or open "Setup tasks...", which you can find a menu at the right bottom corner at the green plus sign, to create a new bash in Cmder.

Create a new task or bash by clicking on the + sign. And fill out some text boxes:
- Enter a name for your task e.g. "Git bash".
- At the big text box enter the path to your Git for Windows installation. You have two possibilities on how to setup up the path:

~~~
""C:\Program Files\Git\bin\sh.exe" --login -i"
~~~

Choose this if you setup Git for Windows with "Use Git from Git bash only" or "Git from the command line and also 3rd-party software" when you had to adjust your PATH environment during the Git for Windows installation.

OR:

~~~
"sh --login -i"
~~~

Choose this if you have chosen "Use Git and optional Unix tools from the Command Prompt" during the Git for Windows installation.

![git-installation-adjusting-path-environment][git-installation-adjusting-path-environment]

The most common settings could look like this:

![cmder-git-bash-settings][cmder-git-bash-settings]

[git-installation-adjusting-path-environment]: /img/2020-09-01-setting-up-cmder-with-git/git-installation-adjusting-path-environment.png "Three options when Adjusting the PATH Environment during the Git for Windows installation."

[cmder-git-bash-settings]: /img/2020-09-01-setting-up-cmder-with-git/cmder-git-bash-settings.png "The most common settings for Cmder when setting up a git bash."

- At last you can give your bash an icon. Type in the following at the "Task parameters" text box:

~~~
/icon "C:\Program Files\Git\mingw64\share\git\git-for-windows.ico"
~~~
