---
layout: default
title: Terminal 
nav_order: 2
parent: Environment Setup
---
## The Shell 
<!--text taken from Intro to Unix Shell research commons workshop url: https://ubc-library-rc.github.io/intro-shell/content/01-what-is-the-shell.html-->
The shell (sometimes referred to as the “Unix shell” after the operating system where it was first developed) is a program that allows you to interact with your computer using typed text commands. For Mac and Linux, which are Unix based systems, you can access the Unix shell through an application called “Terminal”. It is findable like any other piece of software installed on your computer. For Windows 10 users, the Unix shell needs to be turned on but is available as a part of the operating system. You can find more information in [Simplified Installation](https://learn.microsoft.com/en-us/windows/wsl/install#simplified-installation-for-windows-insiders). 
    
### Download Mapbox GL
1. Make sure you are using the bash shell. Run the command ```echo $0``` to check. If your shell is zsh, run ```chsh -s /bin/bash```, then quit and re-open the terminal.     
2. Copy & paste the following command into your terminal. Then hit return to run the command. 

Input
{: .label .label-green }
```sh
$ npm install --save mapbox-gl
```
    
    
 <br>      
If you are experiencing technical issues it is likely due to the way your computer is configured. Use Mapbox's [installation guide](https://docs.mapbox.com/mapbox-gl-js/guides/install/) to help troubleshoot. 