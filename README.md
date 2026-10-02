# Windows WindowMetrics Tweaks (Small Screens / 720p)

Batch scripts to reduce title bar height, scrollbar size, and system font sizes on Windows.  
Especially useful on **720p** and other small screens where every pixel of usable space matters.

## What these scripts do

### `set_windowmetrics_fonts.bat`
Applies the following changes under  
`HKEY_CURRENT_USER\Control Panel\Desktop\WindowMetrics`:

**Sizes**
| Value            | New value |
|------------------|-----------|
| CaptionHeight    | -270      |
| CaptionWidth     | -270      |
| ScrollHeight     | -80       |
| ScrollWidth      | -80       |

**Fonts** (Segoe UI)
| Element          | Size | Style  |
|------------------|------|--------|
| Title Bar        | 8    | Bold   |
| Menu             | 8    | Bold   |
| Message box      | 9    | Regular|
| Palette title    | 8    | Bold   |
| Icon             | 8    | Bold   |
| Tooltip / Status | 8    | Bold   |

### `restore_windowmetrics_defaults.bat`
Restores common Windows defaults:

- CaptionHeight / CaptionWidth → `-330`
- ScrollHeight / ScrollWidth → `-255`
- All six fonts → Segoe UI ≈ 9 pt Regular

## Why use this?

On low-resolution displays (especially **720p**), the default large title bars, thick scrollbars and bigger fonts waste a lot of vertical and horizontal space.  
Reducing these values gives noticeably more room for content.

**Tested and recommended for 720p resolutions** where screen real-estate is limited.

## How to use

1. Download the `.bat` files.
2. Right-click the desired script → **Run as administrator**.
3. Log off and log back in (or restart Explorer) for the changes to take effect.

> **Tip**: Always run the restore script first if you want to go back to defaults.

## Notes

- Changes are per-user (`HKCU`).
- Works on Windows 10 and Windows 11.
- Some modern UWP / WinUI apps may ignore classic WindowMetrics settings.
- Always create a System Restore point or export the `WindowMetrics` key before applying.

## License

Public domain / free to use and modify.
