# NOVADUST Windows Terminal Theme - Implementation Plan

## Overview
Convert the NOVADUST VS Code theme to a Windows Terminal color scheme that can be imported and used in Windows Terminal.

## Theme Analysis

### NOVADUST Color Palette
Based on the VS Code theme, here are the key colors extracted:

#### Background Colors
- **Primary Background**: `#1d2833` (dark blue-gray)
- **Secondary Background**: `#273341` (slightly lighter blue-gray)
- **Tertiary Background**: `#303f51` (selection/hover states)
- **Deep Background**: `#18222b` (darkest shade)

#### Foreground Colors
- **Primary Foreground**: `#cfd1d1` (light gray)
- **Bright Foreground**: `#f7f5e9` (off-white)
- **Muted Foreground**: `#74859a` (blue-gray)
- **Accent Foreground**: `#eeead1` (warm white)

#### ANSI Colors (from terminal section)
The theme already defines ANSI colors for terminals:

**Normal Colors:**
- Black: `#000911`
- Red: `#ff695d`
- Green: `#b9e678`
- Yellow: `#ffd580`
- Blue: `#5fcbc3`
- Magenta: `#d689e3`
- Cyan: `#85dda2`
- White: `#f7f5e9`

**Bright Colors:**
- Bright Black: `#596d84`
- Bright Red: `#ff695d`
- Bright Green: `#b9e678`
- Bright Yellow: `#ffd580`
- Bright Blue: `#5fcbc3`
- Bright Magenta: `#d689e3`
- Bright Cyan: `#85dda2`
- Bright White: `#f7f5e9`

#### Accent Colors
- **Cursor**: `#ffd580` (yellow)
- **Selection**: `#303f51` (blue-gray with transparency)
- **Orange**: `#ffa161`
- **Teal**: `#5fcbc3`
- **Green**: `#85dda2`

## Windows Terminal Color Scheme Structure

Windows Terminal uses a JSON-based color scheme with the following properties:

```json
{
  "name": "Theme Name",
  "background": "#RRGGBB",
  "foreground": "#RRGGBB",
  "cursorColor": "#RRGGBB",
  "selectionBackground": "#RRGGBB",
  
  "black": "#RRGGBB",
  "red": "#RRGGBB",
  "green": "#RRGGBB",
  "yellow": "#RRGGBB",
  "blue": "#RRGGBB",
  "purple": "#RRGGBB",
  "cyan": "#RRGGBB",
  "white": "#RRGGBB",
  
  "brightBlack": "#RRGGBB",
  "brightRed": "#RRGGBB",
  "brightGreen": "#RRGGBB",
  "brightYellow": "#RRGGBB",
  "brightBlue": "#RRGGBB",
  "brightPurple": "#RRGGBB",
  "brightCyan": "#RRGGBB",
  "brightWhite": "#RRGGBB"
}
```

## Color Mapping Strategy

### Direct Mappings
These colors can be directly mapped from the VS Code theme:

| Windows Terminal Property | VS Code Color | Hex Value |
|--------------------------|---------------|-----------|
| `name` | - | "NOVADUST" |
| `background` | `editor.background` | `#1d2833` |
| `foreground` | `terminal.foreground` | `#cfd1d1` |
| `cursorColor` | `editorCursor.foreground` | `#ffd580` |
| `selectionBackground` | `terminal.selectionBackground` | `#303f5156` |
| `black` | `terminal.ansiBlack` | `#000911` |
| `red` | `terminal.ansiRed` | `#ff695d` |
| `green` | `terminal.ansiGreen` | `#b9e678` |
| `yellow` | `terminal.ansiYellow` | `#ffd580` |
| `blue` | `terminal.ansiBlue` | `#5fcbc3` |
| `purple` | `terminal.ansiMagenta` | `#d689e3` |
| `cyan` | `terminal.ansiCyan` | `#85dda2` |
| `white` | `terminal.ansiWhite` | `#f7f5e9` |
| `brightBlack` | `terminal.ansiBrightBlack` | `#596d84` |
| `brightRed` | `terminal.ansiBrightRed` | `#ff695d` |
| `brightGreen` | `terminal.ansiBrightGreen` | `#b9e678` |
| `brightYellow` | `terminal.ansiBrightYellow` | `#ffd580` |
| `brightBlue` | `terminal.ansiBrightBlue` | `#5fcbc3` |
| `brightPurple` | `terminal.ansiBrightMagenta` | `#d689e3` |
| `brightCyan` | `terminal.ansiBrightCyan` | `#85dda2` |
| `brightWhite` | `terminal.ansiBrightWhite` | `#f7f5e9` |

### Note on Selection Background
The VS Code theme uses `#303f5156` which includes alpha transparency (56 in hex = ~34% opacity). Windows Terminal supports transparency in selection backgrounds, so this can be used directly.

## Implementation Steps

### 1. Create the Theme File
Create a JSON file named `novadust-windows-terminal.json` with the complete color scheme.

### 2. Installation Instructions
The theme can be imported into Windows Terminal in two ways:

#### Method 1: Manual Installation
1. Open Windows Terminal
2. Press `Ctrl+,` to open Settings
3. Click "Open JSON file" in the bottom-left corner
4. Locate the `"schemes"` array in the JSON file
5. Add the NOVADUST color scheme to the array
6. Save the file

#### Method 2: Direct Settings UI
1. Open Windows Terminal Settings
2. Go to "Color schemes"
3. Click "Add new"
4. Manually enter each color value

### 3. Apply the Theme
After installation:
1. Go to Settings > Profiles > Defaults (or specific profile)
2. Click "Appearance"
3. Under "Color scheme", select "NOVADUST"
4. Save changes

## Deliverables

1. **novadust-windows-terminal.json** - The complete Windows Terminal color scheme
2. **README-windows-terminal.md** - Installation and usage instructions
3. **color-reference.md** - Complete color palette reference with visual examples

## Additional Considerations

### Transparency Support
Windows Terminal supports:
- Background transparency (acrylic effect)
- Selection background transparency
- These can be configured per-profile in addition to the color scheme

### Profile-Specific Settings
Users can customize:
- Font family and size
- Cursor shape (bar, vintage, underscore, filled box, empty box)
- Background image or video
- Acrylic transparency level

### Testing Recommendations
Test the theme with:
- PowerShell
- Command Prompt
- WSL (Ubuntu, Debian, etc.)
- Git Bash
- Various CLI tools (npm, git, docker, etc.)

## Color Philosophy

The NOVADUST theme follows a "dark blue inspired by the stars" philosophy:
- **Dark blue-gray backgrounds** create a calm, focused environment
- **Warm accent colors** (yellows, oranges) provide contrast without being harsh
- **Cool accent colors** (teals, cyans, greens) complement the blue base
- **Muted foreground colors** reduce eye strain during long coding sessions
- **Bright highlights** for important elements (cursor, selections, errors)

## Future Enhancements

Potential additions:
1. Create variants (e.g., NOVADUST Light, NOVADUST Contrast)
2. Add theme to Windows Terminal theme gallery
3. Create matching themes for other terminals (iTerm2, Alacritty, Hyper)
4. Provide color palette exports for design tools (Figma, Adobe XD)
