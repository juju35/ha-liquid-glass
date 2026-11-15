# Changelog

## 1.0.2 - 2026-11-15

### Fixes
- Semantic state colors (warning, success, error, info) are now darker in light mode so light accents like amber and yellow stay legible on the glass cards, and kept vivid in dark mode.

## 1.0.1 - 2026-11-15

### Fixes
- More-info and other dialogs are now readable: their surface is nearly opaque and the dashboard behind them is blurred and dimmed (`ha-dialog-surface-background`, `dialog-backdrop-filter`, `mdc-dialog-scrim-color`).
- Cards are a little less transparent (0.72 opacity) so the background shows through less and content stays legible.

## 1.0.0 - 2026-11-15

### Features
- Liquid Glass theme for Home Assistant: frosted translucent cards and side panel (`backdrop-filter` blur + saturation) over a soft gray gradient background.
- Light and dark modes, each with its own gray gradient and glass surfaces.
- High-contrast text and icons so cards and panels stay fully legible on the glass.
- Apple-blue accent, 22px rounded cards, translucent app header.
