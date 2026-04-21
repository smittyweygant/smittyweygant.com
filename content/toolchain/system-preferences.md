---
title: 'System Preferences'
date: 2025-02-04T10:00:00+07:00
draft: false
description: 'Documentation of my laptop setup for development & testing'
menus:
  toolchain:
---
Customization of Mac OS System Preferences

* Appearance  
  * Dark Mode  
  * Show Scroll Bars \-\> "Always"  
    * Ugly, but better for web development
<!--more-->  
* Dock  
  * Remove most applications from Dock  
  * Automatic Hide  
  * Smaller Dock  
  * "Show recent applications in Dock" \-\> off  
  * "Show indicators for open applications" \-\> on  
* Display \- Nightshift  
* Security \- Touch ID  
* Notifications \- Off, except for Calendar  
* Siri  
* Trackpad  
  * Tap to Click  
  * Point & Click \-\> Look up & data detectors off  
  * More Gestures \-\> Notification Centre off  
* Keyboard  
  * Text  
    * disable "Capitalise word automatically"  
    * disable "Add full stop with double-space"  
    * disable "Use smart quotes and dashes"  
    * use " for double quotes  
    * use ' for single quotes  
  * Keyboard \-\> Mission Control \-\> disable all  
  * Press FN to \-\> "Do Nothing"  
  * Keyboard Shortcuts \-\> Spotlight \-\> CMD \+ Space disable  
    * We will be using Raycast instead  
* Mission Control  
  * Hot Corners: disable all  
* Finder  
  * General  
    * New Finder windows show: \[Downloads\]  
    * Show these items on the desktop: disable all  
  * Sidebar:  
    * activate all Favorites  
    * move Library to Favorites  
  * Show only:  
    * Desktop  
    * Downloads  
    * Documents  
    * \[User\]  
    * Library  
  * Tags  
    * disable all  
  * Advanced  
    * Show all Filename Extensions  
    * Remove Items from Bin after 30 Days  
    * View \-\> Show Preview (e.g. image files)  
* Sharing  
  * "Change computer name"  
    * Also terminal:  
      * sudo scutil \--set ComputerName "newname"  
      * sudo scutil \--set LocalHostName "newname"  
      * sudo scutil \--set HostName "newname"  
  * "Make sure all file sharing is disabled"  
* Security and Privacy  
  * Turn on FileVault  
  * Add Browser to "Screen Recording"  
* Storage  
  * Remove Garage Band & Sound Library  
  * Remove iMovie  
* Trackpad  
  * Speed: Max  
* Accessibility  
  * Scroll Speed: Max

## MacOS Applications {#macos-applications}

* iMessage  
  * sync iCloud for iMessages just for the sake of syncing, then disable iCloud again  
  * sync contacts on iCloud  
  * iPhone: activate message forwarding to new Mac  
* Pages  
  * show word count  
* Apple Mail  
  * set up all email accounts with [Fastmail](https://join.fastmail.com/9219c0b0) as provider of choice  
  * show most recent message at top  
  * undo send delay set to off  
* Notes  
  * New notes start with: Body  
  * Settings \-\> Disable: Group notes by date  
* Quick Time Player  
  * save to Desktop