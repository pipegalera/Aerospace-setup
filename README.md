# Aerospace setup

My personal config + minimal guide for MacOS Windows Manager app [Aerospace](https://github.com/nikitabobko/AeroSpace)

 <img src="https://raw.githubusercontent.com/nikitabobko/AeroSpace/refs/heads/main/resources/Assets.xcassets/AppIcon.appiconset/icon.png" width="40%" height="40%" align="right">


## Config file

```˙˙˙˙
brew install --cask nikitabobko/tap/aerospace
brew install curl
mkdir ~/.config/aerospace/
curl https://raw.githubusercontent.com/pipegalera/Aerospace-setup/refs/heads/main/aerospace.toml --output ~/.config/aerospace/aerospace.toml
```

### Move cursor after the window changes

```
on-focus-changed = "move-mouse window-lazy-center"
```

### Add app to an specific Workspace when oppened

In terminal: `aerospace list-apps`

Check the app and assign it to a workspace:

```
[[on-window-detected]]
if.app-id = 'com.apple.Notes'
run = "move-node-to-workspace N"
```

### Check the arrow keys

```
# See: https://nikitabobko.github.io/AeroSpace/commands#focusl…–
alt-j = 'focus left'
alt-k = 'focus down'
alt-i = 'focus up'
alt-l = 'focus right'

# See: https://nikitabobko.github.io/AeroSpace/commands#move
alt-shift-j = 'move left'
alt-shift-k = 'move down'
alt-shift-i = 'move up'
alt-shift-l = 'move right'
```

### Main config

- Move box to fullscreen: `alt-shift-f = 'fullscreen'`
- Increase size left box:`alt-1 = 'resize smart -50'`
- Increase size right box: `alt-2 = 'resize smart +50'`
  

## Box shortcuts

- Move box: `alt-shift-;`
- Move box to fullscreen: `alt-shift-f`
- Increase size left box:`alt-1`
- Increase size right box: `alt-2`
- Service mode: `alt-shift-;`
- Free float a window: i) Go to box, ii) Service Mode, iii) press `h`
- Merge box: i) Go to box, ii) Service Mode, iii) Move box
- Unmerge box: i) Go to box, ii) Move box
- Swith to Accordeon layout: `alt-,`
- Swith to Tiles layout: `alt-/`

## Workspace shortcuts

- Move box to Workspace: `alt-shift-{Workspace letter or number}`

## Main 

- Zed: `alt-Q`
- Browser: `alt-W`
- Terminal: `alt-E`

## Apps

- Outlook: `alt-O`
- Apple Notes: `alt-N`
- Github/Git: `alt-G`
- Zotero: `alt-Z`
