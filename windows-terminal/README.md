# NOVADUST for Windows Terminal

A beautiful dark blue color theme for Windows Terminal - inspired by the stars. ✨

This theme is a direct port of the NOVADUST VS Code theme, maintaining the same color palette and visual aesthetic for a consistent experience across your development environment.

## Preview

The NOVADUST theme features:
- **Dark blue-gray background** (`#1d2833`) for reduced eye strain
- **Warm yellow cursor** (`#ffd580`) for easy tracking
- **Vibrant but balanced ANSI colors** for excellent syntax highlighting
- **Carefully selected accent colors** that complement the blue base

## Installation

### Method 1: Using the JSON File (Recommended)

1. **Locate your Windows Terminal settings file:**
   - Open Windows Terminal
   - Press `Ctrl+Shift+,` (or click the dropdown arrow → Settings)
   - Click "Open JSON file" in the bottom-left corner of the Settings UI
   - This will open `settings.json` in your default text editor

2. **Add the NOVADUST color scheme:**
   - Find the `"schemes"` array in the JSON file
   - Copy the entire contents of [`novadust-windows-terminal.json`](./novadust-windows-terminal.json)
   - Paste it into the `"schemes"` array

   Example:
   ```json
   {
     "schemes": [
       {
         "name": "NOVADUST",
         "background": "#1d2833",
         "foreground": "#cfd1d1",
         "cursorColor": "#ffd580",
         "selectionBackground": "#303f5156",
         "black": "#000911",
         "red": "#ff695d",
         "green": "#b9e678",
         "yellow": "#ffd580",
         "blue": "#5fcbc3",
         "purple": "#d689e3",
         "cyan": "#85dda2",
         "white": "#f7f5e9",
         "brightBlack": "#596d84",
         "brightRed": "#ff695d",
         "brightGreen": "#b9e678",
         "brightYellow": "#ffd580",
         "brightBlue": "#5fcbc3",
         "brightPurple": "#d689e3",
         "brightCyan": "#85dda2",
         "brightWhite": "#f7f5e9"
       }
       // ... other color schemes
     ]
   }
   ```

3. **Save the file** - Windows Terminal will automatically reload the settings

### Method 2: Using the Settings UI

1. Open Windows Terminal Settings (`Ctrl+,`)
2. Click "Color schemes" in the left sidebar
3. Click "Add new" button
4. Enter the name: `NOVADUST`
5. Manually enter each color value from the table below
6. Click "Save"

## Applying the Theme

### To All Profiles (Default)

1. Open Windows Terminal Settings (`Ctrl+,`)
2. Click "Defaults" under "Profiles" in the left sidebar
3. Click "Appearance"
4. Under "Color scheme", select **NOVADUST** from the dropdown
5. Click "Save"

### To a Specific Profile

1. Open Windows Terminal Settings (`Ctrl+,`)
2. Select the profile you want to customize (e.g., PowerShell, Command Prompt, Ubuntu)
3. Click "Appearance"
4. Under "Color scheme", select **NOVADUST** from the dropdown
5. Click "Save"

## Color Reference

### Base Colors

| Property | Color | Hex Value | Usage |
|----------|-------|-----------|-------|
| Background | ![#1d2833](https://via.placeholder.com/15/1d2833/1d2833.png) | `#1d2833` | Terminal background |
| Foreground | ![#cfd1d1](https://via.placeholder.com/15/cfd1d1/cfd1d1.png) | `#cfd1d1` | Default text color |
| Cursor | ![#ffd580](https://via.placeholder.com/15/ffd580/ffd580.png) | `#ffd580` | Cursor color |
| Selection | ![#303f5156](https://via.placeholder.com/15/303f51/303f51.png) | `#303f5156` | Selected text background |

### ANSI Colors (Normal)

| Color | Hex Value | Usage |
|-------|-----------|-------|
| Black | `#000911` | Black text |
| Red | `#ff695d` | Errors, important warnings |
| Green | `#b9e678` | Success messages, additions |
| Yellow | `#ffd580` | Warnings, highlights |
| Blue | `#5fcbc3` | Information, links |
| Purple | `#d689e3` | Special keywords, constants |
| Cyan | `#85dda2` | Strings, secondary info |
| White | `#f7f5e9` | Bright text |

### ANSI Colors (Bright)

| Color | Hex Value | Usage |
|-------|-----------|-------|
| Bright Black | `#596d84` | Comments, muted text |
| Bright Red | `#ff695d` | Critical errors |
| Bright Green | `#b9e678` | Emphasized success |
| Bright Yellow | `#ffd580` | Important highlights |
| Bright Blue | `#5fcbc3` | Emphasized information |
| Bright Purple | `#d689e3` | Special emphasis |
| Bright Cyan | `#85dda2` | Emphasized strings |
| Bright White | `#f7f5e9` | Maximum contrast text |

## Recommended Settings

For the best experience with NOVADUST, consider these additional settings:

### Font Recommendations

```json
{
  "profiles": {
    "defaults": {
      "font": {
        "face": "Cascadia Code",
        "size": 11,
        "weight": "normal"
      }
    }
  }
}
```

Popular font choices that work well with NOVADUST:
- **Cascadia Code** (default, includes ligatures)
- **Fira Code** (excellent ligature support)
- **JetBrains Mono** (designed for developers)
- **Consolas** (classic Windows monospace)
- **Inconsolata** (clean and readable)

### Optional Enhancements

#### Acrylic Transparency
Add a subtle transparency effect:

```json
{
  "profiles": {
    "defaults": {
      "useAcrylic": true,
      "acrylicOpacity": 0.9
    }
  }
}
```

#### Cursor Shape
Customize the cursor appearance:

```json
{
  "profiles": {
    "defaults": {
      "cursorShape": "bar",  // Options: bar, vintage, underscore, filledBox, emptyBox
      "cursorHeight": 25
    }
  }
}
```

#### Padding
Add comfortable padding around the terminal content:

```json
{
  "profiles": {
    "defaults": {
      "padding": "8, 8, 8, 8"
    }
  }
}
```

## Compatibility

- **Windows Terminal**: Version 1.4 or later
- **Windows Terminal Preview**: All versions
- **Tested with**: PowerShell, Command Prompt, WSL (Ubuntu, Debian), Git Bash

## Troubleshooting

### Theme not appearing in the dropdown
- Ensure the JSON is valid (no syntax errors)
- Restart Windows Terminal completely
- Check that the theme name is unique

### Colors look different than expected
- Ensure your terminal is using the NOVADUST color scheme
- Check if any profile-specific overrides are applied
- Verify that no other color settings are conflicting

### Selection background not transparent
- Windows Terminal supports alpha transparency in hex colors
- The format is `#RRGGBBAA` where AA is the alpha channel
- `#303f5156` = RGB(48, 63, 81) with ~34% opacity

## Related Themes

- **NOVADUST for VS Code** - The original theme this is based on
- **NOVADUST for iTerm2** - Coming soon
- **NOVADUST for Alacritty** - Coming soon

## Contributing

Found an issue or have a suggestion? Please open an issue or submit a pull request!

## License

This theme is part of the NOVADUST project. See the main repository for license information.

---

**Enjoy coding under the stars!** ✨🌙
