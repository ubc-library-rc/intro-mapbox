---
layout: default
title: Environment Setup
nav_order: 2
has_children: false
---
# Setting up a Developer Environment
In order to write the code that builds and renders your web maps you need a few things.

1. First and foremost, you'll need access to internet connection and a computer with an internet browser installed. Recent versions of [Mozilla Firefox](https://www.mozilla.org) and [Google Chrome](https://www.google.com/chrome/) are the recommended browsers. _Note: this workshop requires that you download software from the internet onto your computer. If you are using a computer that is **not** your personal device, make sure you have permission to make such changes and are able to delete them when done._ 
2. To work with Mapbox you must [sign up](https://account.mapbox.com/auth/signup/) for a free account and [create an access token](https://account.mapbox.com/access-tokens/). 
<!-- 3. Downloading the Mapbox GL JS graphics library requires running one simple command in your computer's terminal. If you have never worked in the terminal, consider browsing the Research Common's introductory workshop [here](https://ubc-library-rc.github.io/intro-shell/content/01-what-is-the-shell.html).-->
3. Lastly, if you haven't already, you should download a [source code editor](https://en.wikipedia.org/wiki/Source_code_editor) for swift and efficient map construction. Much like a word processor helps with writing essays, a code editor makes writing code easier by formatting and color coding your work as you type.  




## Create a Mapbox Account and Access Token
Mapbox's service model is based on a paid subscription, but they offer a free service tier for those interested in using their products for learning, with enough resources to get you started. Use of services is authorized on a user-basis by an **access token.** 

[Sign up](https://account.mapbox.com/auth/signup/) for a free Mapbox account using an email address you have access to (you will be asked to verify your email). 

[Create access token](https://account.mapbox.com/access-tokens/) by giving it a name (like mapbox-workshop) and scrolling to the end of the page where a button says **Create Token**. You will be prompted to confirm your site password. A new access token should appear under the default access token. Keep this browser window open as we will need the access token in a moment. 


## Download a Code Editor 
To make your life easier while viewing or editing code, it's good to use a [source code editor](https://en.wikipedia.org/wiki/Source_code_editor). This workshop recommends [Visual Studio Code](https://code.visualstudio.com/download), but other editors like [Notepad++](https://notepad-plus-plus.org/) or [Sublime Text](https://www.sublimetext.com/3) will work similarly.

It's helpful to see your web-map change as you work. Live Server is an extension for Visual Studio Code that builds a local server to host/render? HTML documents. To install, click the gear icon in the bottom left corner of VS Code and go to extensions. Search for "Live Server" and install. 