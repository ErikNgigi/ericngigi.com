---
title: "Arch Linux Extra Installation"
summary: "This post provides a step-by-step guide on what to do after installing the base installation of Archlinux, including configuring the system and installing additional packages."
date: 2023-04-29T09:45:37+03:01
author: "Eric Ngigi"
image: "/images/post/arch/geowaves.png"
tags: ["Arch Linux", "Tutorial"]
---

The sole purpose of this notes is to help me remember my workflow. Here are some of the things I always do.

## Theming

- Icon themes
	+ papirus-icon-theme
	+ tela-icon-theme
	+ tela-circle-icon-theme

- GTK Theme
	+ whitesur-dark
	+ orchis theme

- Qt5 Theme
	+ `qt5ct` with kvantum

- Cursor Theme
	- vimix-cursors

## Shell

Install `zsh` to replace `bash` shell

Install `zsh`:

``````
pacman -S zsh fzf
``````

- `zsh`: a modern replacement for the bash shell
- `fzf`: fuzzy finder

## Daily Apps
- Browser
  + `brave-bin`: Brave Browser

- Media
	+ `mpv`: media player
	+ `clementine`: Graphical music player
	+ `feh` image viewer
	+ `obs`: screen recorder

- Media and Graphics Editing Tools
	+ `gimp`: image manipulation program
	+ `inkscape`: vector graphics editor
	+ `ffmpeg`: video converter
	+ `imagemagick`: image viewing/manipulation program

- Misc
	+ `flameshot`: screenshot tool
	+ `zathura-pdf-mupdf`: as pdf viewer
	+ `redshift`: blue light filter
	+ `mugshot`: personal user details updater
	+ `arandr`: xrandr front-end
	+ `qbittorent`: Graphical bittorent client
	+ `htop`: CLI interactive process viewer
	+ `scrcpy`: android viewing tool
  + `xmind`: mind mapping tool

---

## Grub Configuration

I add the following lines to `GRUB_CMD_LINUX_DEFAULT` to disable the laptop screen after boot. 

Use `xrandr` to determine the id of each screen. 

``````
xrandr -q
``````

``````
GRUB_CMDLINE_LINUX_DEFAULT="loglevel=3 quiet mitigations=off video=VGA-1:e video=LVDS-1:d radeon.dpm=0 radeon.aspm=0 radeon.pcie_gen2=0 radeon.audio=0 radeon.msi=0 nowatchdog"
``````
