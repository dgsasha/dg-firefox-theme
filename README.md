<img src="icon.svg" alt="Firefox GNOME theme" width="128" align="left"/>

# qualia Firefox theme (Forked from [Firefox GNOME theme](https://github.com/rafaelmardojai/firefox-gnome-theme))

<br>

**A Yaru and Libadwaita inspired theme for Firefox**

This theme is supposed to be used with [qualia GTK theme](https://github.com/dgsasha/qualia-gtk-theme).

## Installation

### Installation script
1. Clone this repo and enter folder:
	```sh
	git clone https://github.com/dgmarie/dg-firefox-theme && cd dg-firefox-theme
	```

2. Run installation script
	#### Install script
	```sh
	./install.sh
	```

	##### Script options
	- `-p <profile_name>` *optional*
		- Set custom profile name, for example `e0j6yb0p.default-nightly`.
		- Default: All the profiles found in the firefox folder

	- ` -c <color_name>` *optional*
		- Specify accent color.
		- Options: `orange` `bark` `sage` `olive` `viridian` `prussiangreen` `lightblue` `blue` `purple` `magenta` `pink` `red`.
		- Default: `orange`.

	- ` -s` *optional*
		- Enable symbolic libadwaita style window controls.

	- `-n` *optional*
		- Don't apply theme to the settings pages in Firefox.

## Updating
`git pull` and then run installation script again

## Uninstalling
1. Go to your profile folder. (Go to `about:support` in Firefox > Application Basics > Profile Directory > Open Directory)
2. Remove `chrome` folder.

## Required Firefox preferences
We provide a **user.js** configuration file in `configuration/user.js` that enable some preferences required by this theme to work. 

You should already have this file installed if you followed one of the installation methods, but in any case be sure this preferences are enabled under `about:config`:

- `toolkit.legacyUserProfileCustomizations.stylesheets`

	This preference is required to load the custom CSS in Firefox, otherwise the theme wouldn't work.

- `svg.context-properties.content.enabled`

	This preference is required to recolor the icons, otherwise you will get black icons everywhere.

> For other non essential preferences checkout `configuration/user.js`.

Also though is not obligatory, some weird issues might happen if you don't use the Firefox's default/system theme because the theme is never tested against the Firefox's light or dark theme.

## Enabling optional features
Optional features can be enabled by creating new `boolean` preferences in `about:config`.

1. Go to the `about:config` page 
2. Type the key of the feature you want to enable
3. Set it as a `boolean` and click on the add button
4. Restart Firefox

### Features

- **Hide single tab** `gnomeTheme.hideSingleTab`

	Hide the tab bar when only one tab is open.

	> **Note:** You should move the new tab button out of the tabbar or it will be hidden when there is only one tab. You can rearrange the toolbars doing a right-click on any toolbar and selecting "Customize Toolbar…".

- **Normal width tabs** `gnomeTheme.normalWidthTabs`

	Use normal width tabs as default Firefox.

- **Bookmarks toolbar under tabs** `gnomeTheme.bookmarksToolbarUnderTabs`

	Move Bookmarks toolbar under tabs.

- **Symbolic tab icons** `gnomeTheme.symbolicTabIcons`

	Make all tab icons look kinda like symbolic icons.

- **Hide WebRTC indicator** `gnomeTheme.hideWebrtcIndicator`

	Hide redundant WebRTC indicator since GNOME provides their own privacy icons in the top right.

- **Drag window from headerbar buttons** `gnomeTheme.dragWindowHeaderbarButtons`

	Allow draging the window from headerbar buttons.

	> **Note:** This feature is BUGGED. It can activate the button with unpleasant behavior.

- **Tab center reborn support** `gnomeTheme.extensions.tabCenterReborn`

	Enable the vertical tab trough the extension : [Tab Center Reborn](https://addons.mozilla.org/en-US/firefox/addon/tabcenter-reborn/).

	> **Note:** You also need to copy the contents of the file `configuration/extensions/tab-center-reborn.css` into the settings page of Tabcenter-reborn..
	
## Known bugs

### CSD have sharp corners
See upstream [bug](https://bugzilla.mozilla.org/show_bug.cgi?id=1408360).

#### Wayland fix:
1. Go to the `about:config` page
2. Search for the `layers.acceleration.force-enabled` preference and set it to true.
3. Now restart Firefox, and it should look good!

#### X11 fix:
1. Go to the `about:config` page 
2. Type `mozilla.widget.use-argb-visuals`
3. Set it as a `boolean` and click on the add button
4. Now restart Firefox, and it should look good!

## Credits :)
### A huge thanks to:
### [Ubuntu](https://ubuntu.com/) for [Yaru](https://github.com/ubuntu/yaru), [vinceliuice](https://github.com/vinceliuice) for [WhiteSur-gtk-theme](https://github.com/vinceliuice/WhiteSur-gtk-theme), [rafaelmardojai](https://github.com/rafaelmardojai) for [firefox-gnome-theme](https://github.com/rafaelmardojai/firefox-gnome-theme)

The Yaru icon assets are licensed under the terms of the [Creative Commons Attribution-ShareAlike 4.0 License](https://creativecommons.org/licenses/by-sa/4.0/).
