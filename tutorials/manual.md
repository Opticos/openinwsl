---
layout: default
title: OpenInWSL Manual
permalink: /tutorials/manual.html
---
## Table of Contents
1.  [Prerequisites](#prerequisites)
2.  [Installing OpenInWSL](#installing-openinwsl)
3.  [Using OpenInWSL](#using-openinwsl)
4.  [Using OpenInWSL Configuration Files](#using-openinwsl-configuration-files)
5.  [Finding Logs](#finding-logs)
6.  [Troubleshooting](#troubleshooting)


***

## OpenInWSL Manual

### Prerequisites ###

OpenInWSL requires [Windows 10 version 2004](https://support.microsoft.com/en-us/help/4028685/windows-10-get-the-update). If you do not have it, please update Windows to continue.

Once Windows is up to date, be sure you have the WSL feature installed and configured properly. Here are some helpful links:
*  [Familiarizing Yourself With WSL](https://docs.microsoft.com/en-us/windows/wsl/about)
*  [Enabling WSL and Installing Distros](https://docs.microsoft.com/en-us/windows/wsl/install-win10)

To make sure WSL is installed correctly, type ```wsl.exe``` in the command line and verify that there are no errors.

You also need an XServer like [GWSL (Recommended)](https://opticos.github.io/gwsl) to provide graphics functionality in WSL. Wslg also works.

### Installing OpenInWSL ###

OpenInWSL can be easily installed from the Microsoft Store. If it is not already installed, get it [here](ms-windows-store://pdp/?productid=9ngmqpwcg7sf) or [here](https://www.microsoft.com/en-us/p/openinwsl/9ngmqpwcg7sf). (Coming Soon)

Note: Some Antiviruses might detect OpenInWSL and block its installation. This is a known bug in Pyinstaller, the program I use to package OpenInWSL. If this occurs, you might want to disable the Antivirus during installation.

### Using OpenInWSL ###
#### Tutorial Video
<div class="iframe-container">
  <iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/8SPFVe47qYA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

OpenInWSL lets you set WSL Linux apps as file handlers in Windows.

#### Steps to use OpenInWSL

1. To setup and association, simply right click a file in Windows Explorer and select "Open In WSL". You can also use the "Open With" menu to make a certain file type always always open in WSL.
2. The first time any specific file type is opened using OpenInWSL, the Association Editor will appear.
3. Select the distro where your WSL app is installed.
4. Enter the command to launch the app or quickly find it using the "App List" button.
5. You can use any custom arguments after your command. If the file's path is not the last argument, specify its position with the ```#fpth#``` variable. Ex. ```gedit #fpth# --new-window```.
6. You can use the manpage button at any time to open the current command's manual page.
7. Test your configuration and save. 
8. Now, when OpenInWSL encounters this file type, it will know how to handle it in WSL.
9. You can use the "Manage File Associations" button to edit your associations after they have been created.

### Using OpenInWSL Configuration Files ###

#### Opening the Settings File
To open the settings file, launch OpenInWSL and click "Configuration File".

Everything in the settings file is exposed in the OpenInWSL GUI.

### Finding Logs ###

#### Reporting a bug? Here is how to find bug reports and logs
1.  Open Windows Explorer.

2.  In the path entry box, paste ```%AppData%/OpenInWSL/```and hit enter.

3.  The logs are stored in ```main.log```.

4.  Include these logs in support emails or share them in the [Discord help server](https://discord.gg/VkvNgkH). Make sure no personal information is contained in them before sharing.


### Troubleshooting ###

Not here yet. Check the OpenInWSL Source Github issues list.

