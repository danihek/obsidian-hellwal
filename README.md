# obsidian-hellwal

## Hellwal

Setup hellwal according to README here: https://github.com/danihek/hellwal

And add (obsidian-theme.css)[./obsidian-theme.css] to your `~/.config/hellwal/templates/` folder.

## Obsidian

Go to your obsidian vault folder, then:

```sh
cd .obsidian
mkdir themes
git clone https://github.com/danihek/obsidian-hellwal Hellwal
```

Create a script and run hellwal with your wallpaper:

```sh
#!/usr/bin/env bash


# Folder with wallpapers
wallpaper_dir=$HOME/wallpapers

# Run hellwal to generate colors and process templates files
hellwal -i $wallpaper_dir -r

# Fetch colors and variables like $wallpaper etc
source ~/.cache/hellwal/variables.sh

# Obsidian - Copy generated theme to obsidian vault folder
cp ~/.cache/hellwal/obsidian-theme.css ~/dox/school-notes/.obsidian/themes/Hellwal/theme.css
```
Now you can go to obsidian settings and select hellwal from themes. Every time you run this script it will automatically update.
