[RC2 of v2.0 available!](https://audioswitch.googlecode.com/files/AudioSwitch%20v2.0%20RC2%20-%20Setup%20%2B%20Zipped%20%2B%20source.zip)
Contains:
Setup for easy install, zipped AudioSwitch for portable/manual install, Source code package

PS: pressing F1 when the list is open launches the settings window!

changes:

Added Mouse Wheel Volume Scrolling :)

some small fixes

Please create an issue for any possible errors - I'd like to get as much bugs out from the release as possible :)


![https://audioswitch.googlecode.com/svn/wiki/demo.png](https://audioswitch.googlecode.com/svn/wiki/demo.png) ![https://audioswitch.googlecode.com/svn/wiki/demo-mic.png](https://audioswitch.googlecode.com/svn/wiki/demo-mic.png)

See  [changelog](https://audioswitch.googlecode.com/svn/wiki/changelog.txt) for recent updates!

[![](https://www.paypal.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=3X7L4G8Y9CUUG)

### Requirements ###
  * Windows 7 or newer, 32bit or 64bit
  * .NET 4.0 Framework
  * Supports both normal and medium DPI settings

### Installation ###
  1. [Download](https://audioswitch.googlecode.com/files/AudioSwitch%20v1.42.zip) latest version and extract the contents to your desired folder.
  1. Start AudioSwitch.exe (create shortcut to Start-> All Programs-> Startup if you like)

### Usage ###
  * **Left-Click** shows menu with available output devices, current default is the selected one in the list.
  * **Ctrl + Left-Click** shows recording devices and allows to switch between them with same behavior.
  * **Mouse Scroll** changes volume of the current device when the menu is visible.

  * **Right-Click** quick-switches the default device to the next available one with a notification balloon (looping-through logic).
  * **Ctrl + Right-Click** quick-switches the recording device.

  * **Alt + Left-Click** toggles mute for current output device.
  * **Ctrl + Alt + Left-Click** toggles mute for recording device.
  * **Right-Click on volume track or handle** toggles mute - indicator of enabled mute is red highlight around volume handle and tray icon with a white x.

  * **Hot Key** - hold down any combination of **Control/Alt/Shift + key** for 5 seconds while AudioSwitch menu is opened. Holding **Delete** key disables the hot key. Any combination is saved and re-applied on startup.
  * **Shift + Left/Right-Click** closes the app.

### Command-line options ###
![https://audioswitch.googlecode.com/svn/wiki/cmd.png](https://audioswitch.googlecode.com/svn/wiki/cmd.png)
  * **-s** - turns on silent mode - only tray icon, no GUI or notifications(except changing or removing hot key combination).
  * **-m _key(s)_** -- will set these keys (Control,Alt,Shift) as modifier keys for a hot key.
  * **-k _key_** -- will set this key as hot key (in combination with modifier key(s)).
  * **-l** - 0-based list of available devices with their respective indexes, exits after list.
  * **-i _n_** - set _n_'th device in list as default output. **Will run AudioSwitch after change.**
  * **-x** - exits AudioSwitch after any of these commands. Hot key combination will **not** be applied when **-x** is used!

Execution sequence is the same as the order of commands.

Examples:
  1. **AudioSwitch.exe -s** -- will run AudioSwitch in silent mode.
  1. **AudioSwitch.exe -i 1** -- will change 1'th device as default and run AudioSwitch.
  1. **AudioSwitch.exe -i 0 -x** -- will change 0'th device as default and exit.
  1. **AudioSwitch.exe -l -i 0 -x** -- will show device list, set 0'th device as default and exit.
  1. **AudioSwitch.exe -i 1 -m control,Alt -k c** -- will set 1'th device as default, set hot key to Control + Alt + C and run AudioSwitch.
  1. **AudioSwitch.exe -m Control,alt -k h -x** -- will **not** change hot key combination, just exits.
  1. **AudioSwitch.exe -x -i 1** -- will **not** do anything.

---

AudioSwitch is started from several similar projects and developed further to fit my personal vision of the final solution. Here are the sources which are used:
  1. http://www.codeproject.com/Articles/18520/Vista-Core-Audio-API-Master-Volume-Control - base library to interface between devices and C#. All copyright notices remain in files but I have removed/modified/optimized a lot of the code in some way.
  1. http://hardforum.com/showthread.php?t=1656534 - main start-up ideas and code for the initial GUI. I disassembled the GUI exe to get the initial code for the popup; I hope the original author/OP don't mind ;)

---

![http://www.jetbrains.com/resharper/img/rs179x67.gif](http://www.jetbrains.com/resharper/img/rs179x67.gif)