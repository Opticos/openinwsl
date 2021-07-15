---
layout: default
title: OpenInWSL Manual
permalink: /tutorials/manual.html
---
## Table of Contents
1.  [Prerequisites](#prerequisites)
2.  [Installing OpenInWSL](#installing-openinwsl)
3.  [Using OpenInWSL](#using-openinwsl)
4.  [Getting Linux File Handler Apps on WSL](#configuring-a-wsl-distro-for-use-with-gwsl)
5.  [Using OpenInWSL Configuration Files](#using-openinwsl-configuration-files)
6.  [Finding Logs](#finding-logs)
7.  [Troubleshooting](#troubleshooting)


***

## OpenInWSL Manual

### Prerequisites ###

OpenInWSL requires [Windows 10 version 2004](https://support.microsoft.com/en-us/help/4028685/windows-10-get-the-update). If you do not have it, please update Windows to continue.

Once Windows is up to date, be sure you have the WSL feature installed and configured properly. Here are some helpful links:
*  [Familiarizing Yourself With WSL](https://docs.microsoft.com/en-us/windows/wsl/about)
*  [Enabling WSL and Installing Distros](https://docs.microsoft.com/en-us/windows/wsl/install-win10)

To make sure WSL is installed correctly, type ```wsl.exe``` in the command line and verify that there are no errors.

You also need an XServer like [GWSL (Recommended)]("https://opticos.github.io/gwsl") to provide graphics functionality in WSL. Wslg also works.

### Installing OpenInWSL ###

OpenInWSL can be easily installed from the Microsoft Store. If it is not already installed, get it [here](ms-windows-store://pdp/?productid=9NL6KD1H33V3) or [here](https://www.microsoft.com/en-us/p/gwsl/9nl6kd1h33v3). (Coming Soon)

Note: Some Antiviruses might detect OpenInWSL and block its installation. This is a known bug in Pyinstaller, the program I use to package OpenInWSL. If this occurs, you might want to disable the Antivirus during installation.

### Using OpenInWSL ###
#### Tutorial Video
<div class="iframe-container">
  <iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/8SPFVe47qYA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>


### Using OpenInWSL Configuration Files ###

#### The GWSL blacklist configuration option allows users to block certain applications and distros from showing up in the app launcher and machine chooser.
1.  Open Windows Explorer.

2.  In the path entry box, paste ```%AppData%/GWSL/```and hit enter.

3.  The configuration file is called ```settings.json```.

4.  Stop the GWSL Service and open this file in your favorite text editor to make changes.

#### Blocking Distros

In the settings file, add the phrases you want blocked to the ```distro_blacklist``` list.

#### Blocking Apps

In the settings file, add the phrases you want blocked to the ```app_blacklist``` list.

##### Note: The format for the blacklists is ```["name1", "name2", "name3"]```. Commas are required between entries.

#### Changing the position of the GWSL Dashboard

The Dashboard in GWSL 1.3.6 can now be configured to pop up on the left side of the desktop. To access this option, open the configuration file and edit the ```"start_menu_mode"``` variable to be ```true``` (for left) or ```false``` (for default right).

#### Changing the Default Terminal App

You can use CMD or the new Windows Terminal. In the settings file, change the value of ```"shell_gui"``` to ```"wt"``` to use Windows Terminal or use ```"cmd"``` to use CMD.

#### Disabling Acrylic for Compatibility with HDR Displays

The GWSL Dashboard does not always display properly when HDR is on (on certain displays). To fix this, open the settings file and set the value of ```"acrylic_enabled"``` to ```false```.


### Finding Logs ###

#### Reporting a bug? Here is how to find bug reports and logs
1.  Open Windows Explorer.

2.  In the path entry box, paste ```%AppData%/OpenInWSL/```and hit enter.

3.  The logs are stored in ```main.log```.

4.  Include these logs in support emails or share them in the [Discord help server](https://discord.gg/VkvNgkH). Make sure no personal information is contained in them before sharing.


### Troubleshooting ###

Not here yet. Check the OpenInWSL Source Github issues list.

