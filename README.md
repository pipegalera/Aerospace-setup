# Aerospace setup

My personal config + minimal guide for MacOS Windows Manager app [Aerospace](https://github.com/nikitabobko/AeroSpace)

![logo](https://raw.githubusercontent.com/nikitabobko/AeroSpace/refs/heads/main/resources/Assets.xcassets/AppIcon.appiconset/icon.png)

## Config file

```˙˙˙˙
brew install --cask nikitabobko/tap/aerospace
brew install curl
mkdir ~/.config/aerospace/
curl https://raw.githubusercontent.com/pipegalera/Aerospace-setup/refs/heads/main/aerospace.toml --output ~/.config/aerospace/aerospace.toml
```

### Move cursor with the window change

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
# See: https://nikitabobko.github.io/AeroSpace/commands#focus
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

## Box shortcuts

- Move box: `alt-shift-;`
- Move box to fullscreen: `alt-shift-f = 'fullscreen'`
- Increase size left box:`alt-1 = 'resize smart -50'`
- Increase size right box: `alt-2 = 'resize smart +50'`
- Service mode: `alt-shift-;`
- Merge box: i) Go to box, ii) Service Mode, iii) Move box
- Unmerge box: i) Go to box, ii) Move box
- Swith to Accordeon layout: `alt-,`
- Swith to Tiles layout: `alt-/`

## Workspace shortcuts

- Move box to Workspace: `alt-shift-{Workspace letter or number}`
- Outlook: `alt-O`
- Apple Notes: `alt-N`
