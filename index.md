---
title: 'Home'
description: 'A large-scale expansion mod for Breath of the Wild.'
home: true
header:
  overlay_image: /second-wind/assets/images/splash-image.png
  overlay_filter: 0.3
  overlay_color: "1a1d24"
  cta_label: "Get Started"
  cta_url: "/get-started"
---

::: tip
For complete guides to homebrew and custom firmware for other devices, check out [CFW.Guide](https://cfw.guide).
:::

[Second Wind](https://gamebanana.com/projects/35468) is a large-scale mod which looks to expand The Legend of Zelda: Breath of the Wild. It adds new content to the game, similar to a DLC pack, and provides various overhauls, bug fixes, tweaks and new gameplay elements for players to explore. For more info, check out the [wiki](https://secondwind.fandom.com/wiki/Second_Wind_Wiki).

You can install this mod either on a homebrewed Wii U or on a Windows PC using Cemu, a Wii U emulator. This guide will take you through the necessary steps to prepare your console or PC for modding. Note: We don't support piracy, you must own both a Wii U and a copy of Breath of the Wild.

# Cemu & Controller Setup

Download [Cemu](https://cemu.info/api/cemu_latest.php), click `Download community graphics packs` on the first screen, then press `Next` and hit `Configure input` to start controller setup.

For this guide, I'll be using a Pro Controller, since it works the best, with the simplest setup. PS4 controllers can be used with [DS4Windows](https://ryochan7.github.io/ds4windows-site/) to get full motion control support. Dual JoyCons should work fine when used through [BetterJoy](https://github.com/Davidobot/BetterJoy/releases/). Other controllers (Wired or wireless XBOX controllers, other USB gamepads) generally work fine but don't support motion controls. If you use one of these, you can right click and drag to use motion controls in Cemu with a mouse.
	
Connect your controller to your PC with a wire or Bluetooth. On Switch controllers, this is done by holding down the sync buttons until the lights come on, then pairing with the controller in your Bluetooth settings.
	
Go to `Options > Input settings`. Set the emulated controller to the Wii U GamePad. For Pro Controllers (and probably dual JoyCons), set the controller API to SDL. Otherwise, set it to XInput. Select the Pro Controller in the list (SDL), or the first one that appears (Xinput). Now click on the box for the A button, and press the corresponding buttons on your controllers to bind buttons. Click in the `<profile name>` box, enter a controller profile name, then hit `Create` and close the input configuration.
	
Motion controls on Pro Controllers (and probably dual JoyCons) should just work out of the box. For [DS4Windows](https://ryochan7.github.io/ds4windows-site/) or [BetterJoy](https://github.com/Davidobot/BetterJoy), hover over `Options > GamePad motion source > DSU1`, then set it to `By Slot`.
Note: You may need to turn on the motion server in BetterJoy/DS4Windows to enable motion control.

# Vanilla BOTW Setup

Depending on if you have a physical or digital copy of BOTW, this install process will be a bit different. If you have a physical copy, you'll need to follow the regular [Cemu dumping guide](https://cemu.cfw.guide/dumping-games), then install them as seen in the [game installation guide](https://cemu.cfw.guide/installing-games#games-updates-and-dlc).

If you bought BOTW on the eShop, follow Cemu's [online play guide](https://cemu.cfw.guide/online-play) to get Cemu working on Nintendo's official servers. Once this is done, go to `Tools > Download Manager`. Hit the connect button next to your account. After a little bit, you should see a list of every Wii U game you own on that account. You can download any of them by right clicking and pressing download.
	
At the time of writing (October 31 2021), Cemu is unable to download BOTW's DLC properly. It's fixed in beta builds, but the fix isn't public yet. Until it's fully supported, you'll have to dump it from your console. For this, refer back to the [game dumping guide](https://cemu.cfw.guide/dumping-games). Once dumped, you can install the DLC by following the steps in the [title installation guide](https://cemu.cfw.guide/installing-games#games-updates-and-dlc). If for whatever reason you can't download your digital copy through Cemu, fall back to following the [dumping guide](https://cemu.cfw.guide/dumping-games), as you would a physical copy.

# Optimization and quick setup for vanilla BOTW

Double-click Breath of the Wild to run it. As soon as Link wakes up, save and return to the title screen (Performance will still be bad at this stage, don't be discouraged!). In the bottom right, it should say `Ver. 1.5.0`, and `DLC Ver. 3.0`. If it does, that means that all of the game files have been correctly installed!
	
Go into the graphics settings `(Options > General settings > Graphics)`, and tick the `Async shader compile` box. This will dramatically decrease stuttering, especially when first starting the game.
In the graphics packs menu `(Options > Graphics packs)`, there will be 3 dropdown menus, and 2 options labelled `Enhancements` and `Graphics`. For each option, you can click on the name to change its settings on the right side of the window, and click the box to enable/disable it. Enable the `Graphics` option, then change the settings in it to your liking. Now, expand the `Mods` dropdown. The most important option here is `FPS++`. After playing for a year, I've never once needed to disable this. It gives a massive performance boost, and lets you play the game mostly without issue at up to 60 FPS. The game can be run at higher framerates, but ragdoll physics get weirder as you go higher, and enemies will completely stop being launched if you're at a perfectly stable 60 FPS. (There's a fix for this coming, but it's not out yet).

Play for a bit, and see how it performs. During the first few minutes, there'll be some pop-in and/or lag, which will become far less common as you play the game.

# [BCML](https://github.com/NiceneNerd/BCML) Setup

Run [this](https://github.com/Torphedo/BOTW-ModdingGuide/releases/download/2.1.0/Installer.bat) batch script, and select option 1. Once installed, you can run BCML with the shortcut generated by the script, or by running `bcml` in a command prompt. (NOT the python console)

<YoutubeVideo url="https://www.youtube.com/embed/dS88dToGvt4" />
