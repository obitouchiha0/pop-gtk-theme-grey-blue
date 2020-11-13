#### Modified version of default pop os gtk theme, with some blue accent
-------------------

<p align="center">
 Light
 <img src="https://raw.githubusercontent.com/obitouchiha0/pop-gtk-theme-grey-blue/master/light.png"/>
 Dark
 <img src="https://raw.githubusercontent.com/obitouchiha0/pop-gtk-theme-grey-blue/master/dark.png"/>
</p>


### Required Components
-------------------
Pop supports Gtk+ 3.22.x

 ```
 * Gtk+-3.0             >= 3.22
 * Gtk+-2.0             >= 2.24.30
 * gtk2-engines-pixbuf  >= 2.24.30
 * gtk2-engines-murrine >= 0.98.1
 ```

### Recommendations

- For GTK, use icons alongside [Pop Icon Theme](https://github.com/pop-os/icon-theme)
- For fonts, use:
 > Window Titles: Fira Sans SemiBold 10

 > Interface: Fira Sans Book 10

 > Documents: Roboto Slab Regular 11

 > Monospace: Fira Mono Regular 11


### Installation
----------------------------

###### Note: You must have sassc installed in order to build Pop. Users of 17.04 or later can all build-dependencies using:

```
sudo apt install sassc meson libglib2.0-dev 
```

For making modifications to assets, you will additionally need these two:

```
sudo apt install inkscape optipng
```


1. If previous versions were installed/existed, remove them first.

 ```
 sudo apt remove pop-gtk-theme
 sudo rm -rf /usr/share/themes/Pop*
 rm -rf ~/.local/share/themes/Pop*
 rm -rf ~/.themes/Pop*
 ```

2. Generate the theme files.

```
meson build && cd build
ninja
```

3. Install the theme.

```
ninja install
```

#### Rebuilding after modifications:

You shouldn't need to rebuild the entire theme after modifications. If you make
changes to any GTK3 or GTK2 assets, delete the old rendered copies and use the
`render-assets.sh` script to regenerate those with new ones with your 
modifications. 
