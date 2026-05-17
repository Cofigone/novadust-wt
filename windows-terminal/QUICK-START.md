# NOVADUST Windows Terminal - Quick Start Guide

Get up and running with the NOVADUST theme in under 2 minutes! ⚡

## 🚀 Fast Installation

### Step 1: Copy the Theme
Copy the contents of [`novadust-windows-terminal.json`](./novadust-windows-terminal.json):

```json
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
```

### Step 2: Open Windows Terminal Settings
- Press `Ctrl+Shift+,` in Windows Terminal
- Click **"Open JSON file"** at the bottom-left

### Step 3: Add to Schemes
Find the `"schemes"` array and add the NOVADUST theme:

```json
{
  "schemes": [
    {
      "name": "NOVADUST",
      "background": "#1d2833",
      // ... paste the rest here
    }
  ]
}
```

### Step 4: Apply the Theme
1. Go back to Settings UI (`Ctrl+,`)
2. Click **"Defaults"** under Profiles
3. Click **"Appearance"**
4. Select **"NOVADUST"** from the Color scheme dropdown
5. Click **"Save"**

## ✅ Done!

Your terminal should now have the beautiful NOVADUST theme applied!

## 🎨 Optional Enhancements

### Recommended Font
```json
{
  "profiles": {
    "defaults": {
      "font": {
        "face": "Cascadia Code",
        "size": 11
      }
    }
  }
}
```

### Add Subtle Transparency
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

### Comfortable Padding
```json
{
  "profiles": {
    "defaults": {
      "padding": "8, 8, 8, 8"
    }
  }
}
```

## 🔧 Troubleshooting

**Theme not showing up?**
- Make sure the JSON is valid (no missing commas or brackets)
- Restart Windows Terminal completely
- Check that you added it to the `"schemes"` array

**Colors look wrong?**
- Verify you selected "NOVADUST" in the Color scheme dropdown
- Check if your profile has any color overrides

## 📚 More Information

- [Full README](./README.md) - Complete documentation
- [Color Reference](./COLOR-REFERENCE.md) - Detailed color information
- [Implementation Plan](../plans/windows-terminal-theme-plan.md) - Technical details

## 💡 Tips

1. **Test with different shells**: Try PowerShell, CMD, WSL, Git Bash
2. **Customize per profile**: Apply different settings to different shells
3. **Pair with VS Code**: Use the NOVADUST VS Code theme for consistency
4. **Share your setup**: Take screenshots and share with the community!

---

**Enjoy your new theme!** ✨
