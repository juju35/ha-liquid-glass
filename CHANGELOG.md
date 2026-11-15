# Changelog

## 1.0.6 - 2026-11-15

### Fixes
- Inner boxes / inactive tiles use a slightly deeper gray so they stand out a bit more from the glass cards (light and dark).

## 1.0.5 - 2026-11-15

### Fixes
- Card popups (confirmation dialogs drawn by cards, which use `card-background-color`) are readable again: `card-background-color` is now an opaque surface, while cards keep their translucent glass via `ha-card-background`.

## 1.0.4 - 2026-11-15

### Fixes
- Inner boxes in light mode use a soft light-gray fill instead of flat white, so they read as calm panels on the glass rather than stark white blocks.

## 1.0.3 - 2026-11-15

### Fixes
- Inner boxes inside cards (such as the download/upload panels of the box card) are visible again: `secondary-background-color` was too transparent and blended into the glass card, so it is now more opaque in both modes.

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
