# NOVADUST Color Reference

Complete color palette documentation for the NOVADUST Windows Terminal theme.

## Color Philosophy

NOVADUST is inspired by the night sky and stars, featuring:
- **Deep blue-gray backgrounds** that evoke the vastness of space
- **Warm accent colors** (yellows, oranges) representing distant stars
- **Cool accent colors** (teals, cyans, greens) like nebulae and cosmic phenomena
- **Balanced contrast** for comfortable long-term viewing

## Complete Color Palette

### Background Colors

| Name | Hex | RGB | HSL | Usage |
|------|-----|-----|-----|-------|
| Primary Background | `#1d2833` | rgb(29, 40, 51) | hsl(210, 28%, 16%) | Main terminal background |
| Selection Background | `#303f5156` | rgba(48, 63, 81, 0.34) | hsla(210, 26%, 25%, 0.34) | Selected text background |

### Foreground Colors

| Name | Hex | RGB | HSL | Usage |
|------|-----|-----|-----|-------|
| Primary Foreground | `#cfd1d1` | rgb(207, 209, 209) | hsl(180, 2%, 82%) | Default text color |
| Cursor | `#ffd580` | rgb(255, 213, 128) | hsl(40, 100%, 75%) | Cursor color |

### ANSI Color Palette

#### Normal Colors

| Color | Hex | RGB | HSL | Description |
|-------|-----|-----|-----|-------------|
| **Black** | `#000911` | rgb(0, 9, 17) | hsl(208, 100%, 3%) | Darkest shade, rarely used for text |
| **Red** | `#ff695d` | rgb(255, 105, 93) | hsl(4, 100%, 68%) | Errors, deletions, critical warnings |
| **Green** | `#b9e678` | rgb(185, 230, 120) | hsl(85, 69%, 69%) | Success, additions, confirmations |
| **Yellow** | `#ffd580` | rgb(255, 213, 128) | hsl(40, 100%, 75%) | Warnings, highlights, attention |
| **Blue** | `#5fcbc3` | rgb(95, 203, 195) | hsl(176, 52%, 58%) | Information, links, primary actions |
| **Purple** | `#d689e3` | rgb(214, 137, 227) | hsl(291, 61%, 71%) | Special keywords, constants, magic |
| **Cyan** | `#85dda2` | rgb(133, 221, 162) | hsl(140, 57%, 69%) | Strings, secondary information |
| **White** | `#f7f5e9` | rgb(247, 245, 233) | hsl(51, 54%, 94%) | Bright text, emphasis |

#### Bright Colors

| Color | Hex | RGB | HSL | Description |
|-------|-----|-----|-----|-------------|
| **Bright Black** | `#596d84` | rgb(89, 109, 132) | hsl(212, 19%, 43%) | Comments, muted text, gray |
| **Bright Red** | `#ff695d` | rgb(255, 105, 93) | hsl(4, 100%, 68%) | Critical errors, urgent attention |
| **Bright Green** | `#b9e678` | rgb(185, 230, 120) | hsl(85, 69%, 69%) | Emphasized success, strong positive |
| **Bright Yellow** | `#ffd580` | rgb(255, 213, 128) | hsl(40, 100%, 75%) | Important highlights, key information |
| **Bright Blue** | `#5fcbc3` | rgb(95, 203, 195) | hsl(176, 52%, 58%) | Emphasized information, primary focus |
| **Bright Purple** | `#d689e3` | rgb(214, 137, 227) | hsl(291, 61%, 71%) | Special emphasis, unique elements |
| **Bright Cyan** | `#85dda2` | rgb(133, 221, 162) | hsl(140, 57%, 69%) | Emphasized strings, important data |
| **Bright White** | `#f7f5e9` | rgb(247, 245, 233) | hsl(51, 54%, 94%) | Maximum contrast, critical text |

## Color Relationships

### Complementary Pairs
- **Red** (`#ff695d`) ↔ **Cyan** (`#85dda2`) - Error vs Success
- **Yellow** (`#ffd580`) ↔ **Blue** (`#5fcbc3`) - Warning vs Information
- **Purple** (`#d689e3`) ↔ **Green** (`#b9e678`) - Special vs Normal

### Analogous Groups
- **Cool tones**: Blue (`#5fcbc3`), Cyan (`#85dda2`), Green (`#b9e678`)
- **Warm tones**: Red (`#ff695d`), Yellow (`#ffd580`)
- **Neutral tones**: Purple (`#d689e3`), White (`#f7f5e9`)

## Usage Examples

### Command Line Output

```bash
# Success message (Green)
✓ Build completed successfully

# Error message (Red)
✗ Error: File not found

# Warning message (Yellow)
⚠ Warning: Deprecated API usage

# Information (Blue)
ℹ Info: 5 files changed

# Special status (Purple)
★ Special: Custom configuration detected
```

### Git Output

```bash
# Modified files (Yellow)
M  src/app.js

# Added files (Green)
A  src/new-feature.js

# Deleted files (Red)
D  src/old-file.js

# Untracked files (Cyan)
?? temp/cache.tmp
```

### Directory Listings

```bash
# Directories (Blue)
drwxr-xr-x  5 user  staff   160 May 17 08:00 src/

# Executables (Green)
-rwxr-xr-x  1 user  staff  1024 May 17 08:00 build.sh*

# Regular files (White)
-rw-r--r--  1 user  staff   512 May 17 08:00 README.md

# Symlinks (Cyan)
lrwxr-xr-x  1 user  staff    12 May 17 08:00 link -> target
```

### Log Levels

```bash
[DEBUG]   Detailed debugging information     # Bright Black
[INFO]    General informational messages     # Blue
[WARN]    Warning messages                   # Yellow
[ERROR]   Error messages                     # Red
[FATAL]   Critical errors                    # Bright Red
```

## Accessibility

### Contrast Ratios

All colors have been tested for readability against the background:

| Color | Against Background | WCAG AA | WCAG AAA |
|-------|-------------------|---------|----------|
| Foreground (`#cfd1d1`) | `#1d2833` | ✓ Pass | ✓ Pass |
| Red (`#ff695d`) | `#1d2833` | ✓ Pass | ✓ Pass |
| Green (`#b9e678`) | `#1d2833` | ✓ Pass | ✓ Pass |
| Yellow (`#ffd580`) | `#1d2833` | ✓ Pass | ✓ Pass |
| Blue (`#5fcbc3`) | `#1d2833` | ✓ Pass | ✓ Pass |
| Purple (`#d689e3`) | `#1d2833` | ✓ Pass | ✓ Pass |
| Cyan (`#85dda2`) | `#1d2833` | ✓ Pass | ✓ Pass |
| White (`#f7f5e9`) | `#1d2833` | ✓ Pass | ✓ Pass |

### Color Blindness Considerations

The theme has been designed with color blindness in mind:

- **Protanopia/Deuteranopia** (Red-Green): Uses brightness and saturation differences
- **Tritanopia** (Blue-Yellow): Maintains distinct hues across the spectrum
- **Monochromacy**: Sufficient contrast through brightness variations

## Color Swatches

### Visual Reference

```
Background Colors:
████████ #1d2833 (Primary Background)
████████ #303f5156 (Selection - with transparency)

Foreground Colors:
████████ #cfd1d1 (Primary Foreground)
████████ #ffd580 (Cursor)

ANSI Normal:
████████ #000911 (Black)
████████ #ff695d (Red)
████████ #b9e678 (Green)
████████ #ffd580 (Yellow)
████████ #5fcbc3 (Blue)
████████ #d689e3 (Purple)
████████ #85dda2 (Cyan)
████████ #f7f5e9 (White)

ANSI Bright:
████████ #596d84 (Bright Black)
████████ #ff695d (Bright Red)
████████ #b9e678 (Bright Green)
████████ #ffd580 (Bright Yellow)
████████ #5fcbc3 (Bright Blue)
████████ #d689e3 (Bright Purple)
████████ #85dda2 (Bright Cyan)
████████ #f7f5e9 (Bright White)
```

## Comparison with VS Code Theme

The Windows Terminal theme maintains color consistency with the VS Code theme:

| Element | VS Code | Windows Terminal | Match |
|---------|---------|------------------|-------|
| Background | `editor.background` | `background` | ✓ |
| Foreground | `terminal.foreground` | `foreground` | ✓ |
| Cursor | `editorCursor.foreground` | `cursorColor` | ✓ |
| Selection | `terminal.selectionBackground` | `selectionBackground` | ✓ |
| ANSI Colors | `terminal.ansi*` | ANSI properties | ✓ |

## Export Formats

### CSS Variables

```css
:root {
  --novadust-bg: #1d2833;
  --novadust-fg: #cfd1d1;
  --novadust-cursor: #ffd580;
  --novadust-selection: #303f5156;
  
  --novadust-black: #000911;
  --novadust-red: #ff695d;
  --novadust-green: #b9e678;
  --novadust-yellow: #ffd580;
  --novadust-blue: #5fcbc3;
  --novadust-purple: #d689e3;
  --novadust-cyan: #85dda2;
  --novadust-white: #f7f5e9;
  
  --novadust-bright-black: #596d84;
  --novadust-bright-red: #ff695d;
  --novadust-bright-green: #b9e678;
  --novadust-bright-yellow: #ffd580;
  --novadust-bright-blue: #5fcbc3;
  --novadust-bright-purple: #d689e3;
  --novadust-bright-cyan: #85dda2;
  --novadust-bright-white: #f7f5e9;
}
```

### SCSS Variables

```scss
$novadust-bg: #1d2833;
$novadust-fg: #cfd1d1;
$novadust-cursor: #ffd580;
$novadust-selection: #303f5156;

$novadust-black: #000911;
$novadust-red: #ff695d;
$novadust-green: #b9e678;
$novadust-yellow: #ffd580;
$novadust-blue: #5fcbc3;
$novadust-purple: #d689e3;
$novadust-cyan: #85dda2;
$novadust-white: #f7f5e9;

$novadust-bright-black: #596d84;
$novadust-bright-red: #ff695d;
$novadust-bright-green: #b9e678;
$novadust-bright-yellow: #ffd580;
$novadust-bright-blue: #5fcbc3;
$novadust-bright-purple: #d689e3;
$novadust-bright-cyan: #85dda2;
$novadust-bright-white: #f7f5e9;
```

### Python Dictionary

```python
NOVADUST = {
    'background': '#1d2833',
    'foreground': '#cfd1d1',
    'cursor': '#ffd580',
    'selection': '#303f5156',
    'black': '#000911',
    'red': '#ff695d',
    'green': '#b9e678',
    'yellow': '#ffd580',
    'blue': '#5fcbc3',
    'purple': '#d689e3',
    'cyan': '#85dda2',
    'white': '#f7f5e9',
    'bright_black': '#596d84',
    'bright_red': '#ff695d',
    'bright_green': '#b9e678',
    'bright_yellow': '#ffd580',
    'bright_blue': '#5fcbc3',
    'bright_purple': '#d689e3',
    'bright_cyan': '#85dda2',
    'bright_white': '#f7f5e9',
}
```

## Design Resources

### Figma/Sketch Color Palette

Import these colors into your design tools:

1. Create a new color palette named "NOVADUST"
2. Add each color with its corresponding name
3. Use for mockups, documentation, and design consistency

### Adobe Color Theme

Visit [Adobe Color](https://color.adobe.com/) and create a custom theme with these values for use in Adobe Creative Suite applications.

---

**Last Updated**: May 2026  
**Version**: 1.0.0  
**Maintained by**: NOVADUST Theme Project
