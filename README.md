# Aerospace setup
Basic config and guide for MacOS app Aerospace


## Config file

```
brew install aerospace curl
echo 'export PATH="/usr/local/opt/curl/bin:$PATH"' >> ~/.zshrc
mkdir && cd ~/.config/aerospace/
curl asd --output ~/.config/aerospace/aerospace.toml
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
