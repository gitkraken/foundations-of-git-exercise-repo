---

title: Themes
description: Using and creating themes in GitKraken Client.

---

# GitKraken Client Themes

***

## Built-in Themes

You can set your GitKraken Client theme by navigating to  <i class="fas fa-cog"></i> <em class='context-menu'>Preferences <i class='fa fa-caret-right'></i> UI Customization</em> menu. 

This can also be done quickly from the <i  class="fa fa-magic" style="transform: rotate(225deg)"></i> [Command Palette](/start-here/command-palette/) (shortcut <kbd>&#8984;</kbd><kbd>P</kbd> or <kbd>Ctrl</kbd><kbd>P</kbd>), typing `switch theme`, and then the name of the theme.

<img src="/img/documentation/getting-started/theme-switch.gif" class="img-bordered img-responsive center">

### Sync with System

If your system is capabale of it, you can set GitKraken Client to match your operating system's current theme. This can be done from the <i class="fas fa-cog"></i> <em class='context-menu'>Preferences <i class='fa fa-caret-right'></i> UI Customization</em> menu or the <i  class="fa fa-magic" style="transform: rotate(225deg)"></i> [Command Palette](/start-here/command-palette/).

***

## Custom Themes

In addition to the default themes, GitKraken Client supports custom user-defined themes. Each of the .jsonc-default theme files you see in this folder can act as a template "base" for your new custom theme.

### Making Your Own Theme

To make your own custom theme, follow these steps:

1. Make a copy of one of the default theme files you'd like to base your custom theme off of in this folder.

2. Rename your copied file to be `MyCustomTheme.jsonc` (i.e. drop the `-default` from the extension and give it a unique name).

3. Open your new theme file in a text editor.

4. Change the `meta.name` property of your theme file to be something unique (a good idea would be to match the file name). The `name` will be used as the display for the option under `Preferences > UI Customization > Theme` in `GitKraken`, so make it something you'll recognize. The scheme must be "light" or "dark", and will be used for default colors if anything is missing. If new properties are added in future releases, your theme will continue to work as-is, by using the scheme to choose a default color for the missing properties.

5. Back in `GitKraken`, find your new custom theme under `Preferences > UI Customization > Theme` and select it.

6. Edit the color values for any of the props under `themeValues`.


<div class='callout callout--basic'>
    <p><strong>Note:</strong> Themes are hot-loaded. That means that as you save color edits to your theme files, you will see the the changes take effect immediately. If at any point your theme file contains an error after you've saved (bad JSON, improper function, improper value), GitKraken will revert to the default `DARK` theme. This is a safety precaution.
</p>
</div>

### Supported CSS/LESS Functions

#### Supported CSS Functions

- calc
- hsl
- hsla
- max
- min
- rgb
- rgba
- var
 
See [CSS functions](https://www.w3schools.com/cssref/css_functions.asp) <i class="fa fa-link"></i> for more details. 
 
#### Supported LESS Functions

- darken
- desaturate
- fade
- lighten
- mix
- mixLess
- saturate

See [LESS functions](https://lesscss.org/functions) <i class="fa fa-link"></i> for more details.