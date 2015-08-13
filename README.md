# kodi-remote-osx-widget
OSX Dashboard Widget to control Kodi, It was originally based on the Boxee widget made by Lot49 (lot49.org), then later updated and modified for XBMC by Topfjoer who has ceesed development.

![](https://raw.githubusercontent.com/grantrutherford/kodi-remote-osx-widget/master/KODI%20Remote.wdgt/Default.png)

For more informtaion please see forum thread - http://forum.kodi.tv/showthread.php?tid=19448

Please feel free make changes or raise issues.

## Installation

Download the zip version, and double click the .wdgt file to install it in your dashboard.

## Features

* Remote control through both the widget buttons AND your keyboard!
* Start KODI via SSH (Not working currently)
* Play a YouTube video link: Drag and drop link or paste link (needs YouTube add-on)
* Exit KODI: Fn+Backspace
* Auto-detection of KODI's virtual keyboard. The widget then automatically shows a text field.
* Keymap for the (US) keyboard:
  * Navigation:	Arrow keys
  * Select:	Enter
  * Back:	Backspace
  * Homescreen:	Esc or h
  * Fullscreen:	Tab or f
  * Play/Pause:	Spacebar
  * Stop:	x or s
  * Fastforward:	. (>)
  * Rewind:	, (<)
  * Skipnext:	= (+)
  * Skipprevious:	-
  * OSD menu:	m
  * Context menu:	c
  * Item info:	i
  * Playlist:	p or l
  * Queue:	q
  * Mute:	\
  * Volume down:	[
  * Volume up: ]	

## Setup

In the settings pane, accessable by clicking the small i in the bottom corner:

1. Fill in the correct ip-address of the computer you're running KODI on.
2. If necessary, change the port number. This widget now uses the WebSocket, NOT the HTTP port! Usually, this value should be kept at default (9090).
3. Finally in KODI do not forget to enable "Allow programs on other systems to control KODI" in "System settings> Services > Remote control"!

## Optional (In progress for KODI)

The widget also has the capability of starting KODI over SSH (using expect) by clicking the KODI logo. This is useful for me personally, because I run KODI on an Ubuntu server. It allows me to remotely start KODI and also to close is down without shutting down the entire system. If you want to use the startup feature you'll need to uninstall any KODI-live and KODI-standalone packages (if present).
To do this, run the following commands in the terminal:
1) sudo apt-get remove --purge KODI-live
2) sudo autoremove
Next, fill in the ssh port of your server (usually 22), the user that will run XBMC, and the password. If you DON'T want to use this feature, just leave the fields "Port SSH", "User" and "Password" blank. Obviously, the 'Host' and 'Port KODI' fields need to be filled in.
