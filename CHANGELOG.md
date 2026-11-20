# Changelog

## 1.1.1 - 2026-11-20

### Fixes
- Status colors are readable as text on the glass, in light and dark mode: every one of them (`green`, `amber`, `orange`, `yellow`, `blue`, `light-blue`, `cyan`, `teal`, `purple`, `deep-purple`, `red`, `grey`, and `success`/`warning`/`error`/`info`, with their `rgb-*`) now reaches a 4.5:1 contrast on the frosted card and its inner tiles, measured over the lightest and darkest stops of the background gradient, and 3:1 as an icon on its tinted pastille. Light mode: green, amber, orange, yellow, blue, light-blue, cyan, teal and grey are darker. Dark mode: orange, blue, light-blue, purple, deep-purple, red and grey are lighter. Hues are unchanged, and ha-neutral uses the same palette.
- Dark mode: the inner tiles (`secondary-background-color`) are a fainter white veil on the glass card (8% instead of 15%); at 15% no red, blue or purple could reach 4.5:1 on them without turning pastel and purple and deep-purple becoming the same color.

### Maintenance
- Validate: a new check computes the contrast of every status color on the theme's frosted card (over the page gradient), tile and dialog backgrounds, in light and dark, and fails below 4.5:1 (text) or 3:1 (icon on its pastille).

## 1.1.0 - 2026-11-20

### Features
- Status palette of the ha-* cards, the same as the ha-neutral theme, in light and dark: `green`, `amber`, `orange`, `yellow`, `blue`, `light-blue`, `cyan`, `teal`, `purple`, `deep-purple`, `red` and `grey-color`, each with its `rgb-*` variable. Home Assistant's state colors (a light on, cooling, media playing…) and the ha-* cards' state lines now read clearly on the light glass, and both ha-* themes tint the cards alike.
- `success`, `warning`, `error` and `info-color` follow that palette (green, amber, red, blue).
- Light amber `#9f691b` and yellow `#8e7109` (with their `rgb-*` and `warning-color`) match ha-neutral's darker values, which reach a 4.5:1 contrast on white.
- Light mode: text on the accent (`text-primary-color`, used on blue buttons and badges) is white, as in Apple's and Home Assistant's own themes, instead of near-black.
- The translucent dashboard header is frosted like the cards (`app-header-backdrop-filter`), so content scrolling under it is blurred instead of showing through.

### Fixes
- Light mode: `rgb-accent-color` now matches the green accent (`#30d158`); it was a different, darker green, so translucent accent tints did not match the accent itself.
- Dark mode: the accent is Apple's dark-mode blue `#0a84ff`, which its `rgb-primary-color`, the selected side-panel item and the active state icons already used.
- `rgb-primary-text-color` is set in both modes, so hovers and ripples tinted with it match the theme's text color.
- Theme file comments in English.

### Maintenance
- Validate: `setup-python` pinned to a commit, and a new check that every `rgb-*` variable matches the color it shadows (an `rgb-*` without its `#rrggbb` color fails too).
- Removed the unused `docs/preview.png` (nothing references it).

## 1.0.8 - 2026-11-15

### Fixes
- Dark mode: secondary text is brighter (opacity 0.8) so card popups and subtitles are easier to read on the dark surfaces.

## 1.0.7 - 2026-11-15

### Changes
- Inactive tiles / inner boxes in light mode use a soft light blue-gray, so they read as calm panels that are clearly distinct from the green active tiles.

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
