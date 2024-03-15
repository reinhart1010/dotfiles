# themer - My Color Set

## Visual Studio

1. Select Tools > Import and Export Settings...
2. Choose the "Import selected environment settings" option
3. Choose whether or not to save a backup of current settings
4. Click "Browse..." and choose the generated theme file ('Visual Studio/themer-my-color-set-dark.vssettings' or 'Visual Studio/themer-my-color-set-light.vssettings')
5. Click "Finish"

## VS Code

Copy (or symlink) the generated package directory into the VS Code extensions directory:

```
cp -R 'VS Code/themer-my-color-set' ~/.vscode/extensions/
```

Then reload or restart VS Code. The generated theme package should be in the list of installed extensions, and "Themer My Color Set Dark" / "Themer My Color Set Light" will be available in the list of themes.

## Xcode

Copy (or symlink) the generated theme files to Xcode's themes directory:

```
mkdir -p ~/Library/Developer/Xcode/UserData/FontAndColorThemes
cp 'Xcode/Themer My Color Set Dark.dvtcolortheme' ~/Library/Developer/Xcode/UserData/FontAndColorThemes/
cp 'Xcode/Themer My Color Set Light.dvtcolortheme' ~/Library/Developer/Xcode/UserData/FontAndColorThemes/
```

Then restart Xcode. The themes will be available in Preferences > Fonts and Colors.

## CMD

Simply double-click the desired theme file to add the color keys to the registry:

* `CMD/themer-my-color-set-dark.reg`
* `CMD/themer-my-color-set-light.reg`

The scheme of CMD can then be configured with the `color` command. For example, use `color 07` to set the background and foreground to your color set's default.

## Konsole

Copy (or symlink) the generated files to `~/.local/share/konsole/`:

```
cp 'Konsole/themer-my-color-set-dark.colorscheme' ~/.local/share/konsole/
cp 'Konsole/themer-my-color-set-light.colorscheme' ~/.local/share/konsole/
```

Then choose the desired theme in Konsole > Settings > Edit Current Profile > Appearance.

## Terminal

1. Launch Terminal.app and open the preferences (`cmd`-`,`)
2. Click Profiles > (...) icon > Import...
3. Choose the generated files (`Terminal/Themer My Color Set Dark.terminal` / `Terminal/Themer My Color Set Light.terminal`)
4. Select the imported theme ("Themer My Color Set Dark" or "Themer My Color Set Light") from the profile picker

## Windows Terminal

1. Open the Windows Terminal settings (`Ctrl`-`,`)
2. Add the contents of 'Windows Terminal/themer-my-color-set-dark.json' and 'Windows Terminal/themer-my-color-set-light.json' to the `schemes` array in `profile.json`
3. Set the `colorScheme` property to the desired scheme name ("Themer My Color Set Dark" or "Themer My Color Set Light") in the profiles section of `profile.json`, e.g.:

```
"profiles": {
  "defaults": {
    "colorScheme": "Themer My Color Set Dark"
  }
}
```

## Chrome

1. Launch Chrome and go to `chrome://extensions`.
2. Check the "Developer mode" checkbox at the top.
3. Click the "Load unpacked extension..." button and choose the desired theme directory (`Chrome/Themer My Color Set Dark` or `Chrome/Themer My Color Set Light`).

(To reset or remove the theme, visit `chrome://settings` and click "Reset to Default" in the "Appearance" section.)

## CSS

Import the generated theme file into your stylesheet via `@import()`, or into your HTML markup via `<link>`.

`hex.css` provides the theme colors in hex format; `rgb.css` and `hsl.css` in RGB and HSL formats respectively along with individual channel values for further manipulation if desired.

Generated files:

* `CSS/Themer My Color Set - hex.css`
* `CSS/Themer My Color Set - rgb.css`
* `CSS/Themer My Color Set - hsl.css`

## Firefox Add-on

To use the generated extension package, the code will need to be packaged up and signed by Mozilla.

To package the code in preparation for submission, the `web-ext` tool can be used:

```
npx web-ext build --source-dir 'Firefox Add-on/Themer My Color Set Dark' # or 'Firefox Add-on/Themer My Color Set Light'
```

Then the package can be submitted to Mozilla for review in the [Add-on Developer Hub](https://addons.mozilla.org/en-US/developers/addon/submit/distribution).

Learn more about Firefox themes from [extensionworkshop.com](https://extensionworkshop.com/documentation/themes/)

To theme Firefox without the need to create a developer account and go through the extension review process, see themer's integration with [Firefox Color](https://color.firefox.com).

## KDE Plasma Colors

1. Open System Settings
2. Navigate to Appearance > Colors
3. Click "Install from File..." and choose the generated theme file (`KDE Plasma Colors/ThemerMyColorSetDark.colors` or `KDE Plasma Colors/ThemerMyColorSetLight.colors`)