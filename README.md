# microsoft-terminal-settings
A collection of profiles, color schemes, and other settings for Windows Terminal

## Windows Terminal
Windows Terminal is a new, modern, feature-rich, productive terminal application for command-line users. It includes support for creating custom color schemes and adding new terminal shells through a `settings.json` file.

### Profiles
A profile specifies a command to execute paired with information about how it should look and feel. Each one of them will appear in the 'New Tab' dropdown.
For more information see the [profile](https://github.com/microsoft/terminal/blob/master/doc/cascadia/SettingsSchema.md#profiles) schema.

To use a profile, copy the JSON text for your desired terminal shell and paste it into the `profiles` section in `settings.json`.

```JSON
"profiles": {
   "list": [
     // Put your profile here...
   ]
}
```
For profiles that have an icon, if the icon is in the `ms-appdata:///roaming/` format, you can copy the icon to the `%USERPROFILE%\AppData\Local\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\RoamingState` folder and it will automatically appear.

### Color schemes
A color scheme specifies the colors used by a terminal shell. One color scheme can be used by multiple terminal shells. For more information on the [color schemes] (https://github.com/microsoft/terminal/blob/master/doc/cascadia/SettingsSchema.md#schemes) schema.

Properties listed below are specific to each color scheme. You can use [ColorTool](https://github.com/microsoft/terminal/tree/master/src/tools/ColorTool) or [terminal.sexy](https://terminal.sexy/) to create and explore new color schemes.

To use a color scheme, copy the JSON text for your desired scheme and paste it into the `schemes` section in `settings.json`.

```JSON
"schemes": [
     // Put your scheme here...
]
```

## Bugs and feature requests
Do you have a bug or a request? Please use the [issue tracker](https://github.com/scottdorman/microsoft-terminal-settings/issues) and search for existing and closed issues. If your problem or request isn't addressed yet, go ahead and [open a new issue](https://github.com/scottdorman/microsoft-terminal-settings/issues/new).

## Contributing
You can also get involved and [fork the repository](https://github.com/scottdorman/microsoft-terminal-settings/fork) to submit your own pull requests.

### Profiles
If you want to create a new profile, use the [_template.json](/profiles/_template.json) file as a starting point and submit a pull request or an issue. Don't include any machine or user specific paths (for things such as startingDirectory), color schemes, fonts, font sizes and things that the end-user might want to personalize for their own environment.

You will also need to set a GUID value. **Don't use the empty GUID value in the template.**

If you want a custom icon, be sure to include it with the issue or pull request and set the icon path to be `ms-appdata:///roaming/file.png` (where `file.png` is the name of your icon file). Be sure images are sized to 32x32 pixels.

### Color schemes
If you want to create a new scheme, use the [_template.json](/color-schemes/_template.json) file as a starting point and submit a pull request or an issue. All colors use hex color format.

## Thanks
- Most of the themes were sourced from [iTerm2-Color-Schemes](https://github.com/mbadolato/iTerm2-Color-Schemes).
- [Microsoft Terminal](https://github.com/microsoft/terminal)
