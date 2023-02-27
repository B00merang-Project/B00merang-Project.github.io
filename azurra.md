---
title: Azurra
layout: page
permalink: /azurra-framework
---

![azurra-logo](https://raw.githubusercontent.com/B00merang-Project/Azurra_framework/assets/azurra_framework.png)

Azurra is an SCSS framework that we developed to make maintaining and creating GTK themes easy and simple.
We achieve this in a couple of ways:
- Modularity: GTK widgets have their styles declared in different files, which makes it easy to add/remove widgets.
- Reusability: Other themes can use another theme's styles in case they have to look similar (ex. Windows Vista and 7).
- Small footprint: You can create a new theme by editing as little as 3 files!
- Flexibility: SCSS makes theme creation very flexible, and some changes (ex. button radius) can be edited from a single file

### Components
- autogen script to parse SCSS to CSS for specified themes
- Bash script to automate repetitive string replacement/insertion/deletion operations
- Rendering subsystem to quickly render SVGs to PNGs
- Python script to check dependencies between themes and detect cross-dependencies

### How it works
Each theme has its own directory with its own configuration files. You can change colors in _colors.scss, or if you want to customize how a GTK widget looks, you can edit its corresponding SCSS file in the /widgets folder. When running the autogen script, SCSS will parse the gtk.scss file into the gtk.css file. If you assigned the 'target_dir' variable in theme.rc, the script will then make a copy of the theme to that folder.

### How to use it
You can visit the [project's wiki](https://github.com/B00merang-Project/Azurra_framework/wiki/) for documentation and a step-by-step tutorial

### Roadmap
Planned for this year (2023):
- GTK4 compatibility (in progress)
- Add Cinnamon themes
- Add Gnome-shell themes

Planned for later:
- Reorganize to support both GTK3 and GTK4 with minimal changes
- Cosmic theme support (when released)

Long-term objectives:
- Support for KDE directly or through a compatible toolkit (ex. Kvantum)
