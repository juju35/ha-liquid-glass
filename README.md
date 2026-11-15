# Liquid Glass — Home Assistant theme

Apple-style *Liquid Glass* theme for Home Assistant: frosted translucent cards and side panel over a soft gray gradient, with light and dark modes. Text and controls stay fully legible on the glass.

![Liquid Glass theme](docs/preview.png)

## Features

- Frosted-glass cards and sidebar (`backdrop-filter` blur + saturation)
- Gray gradient background (light & dark)
- High-contrast text for readability on translucent surfaces
- Apple-blue accent, rounded 22px cards

## Installation

### Marketplace (Home Assistant 2026.11+)

1. **Settings → Marketplace → Add from link**, paste this repository URL.
2. Add this to `configuration.yaml` if not already present:
   ```yaml
   frontend:
     themes: !include_dir_merge_named themes
   ```
3. Restart Home Assistant.
4. **Profile → Theme → Liquid Glass**.

### Manual

Copy `themes/liquid-glass.yaml` into your `config/themes/` folder, then do steps 2–4 above.

## Notes

The glass effect relies on CSS `backdrop-filter`. On some browsers/devices you may need to enable transparency effects. Falls back to a solid translucent color where unsupported.

## License

MIT © juju35
