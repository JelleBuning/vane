# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository overview

This repo contains a single Home Assistant frontend theme, `themes/vane.yaml`, packaged for installation via [HACS](https://hacs.xyz/) (see `hacs.json`) or by manually copying the file into a Home Assistant `themes/` folder. It is not a software project with a build step.

## Development

There is no build, lint, or test tooling in this repo. Changes are made by editing `themes/vane.yaml` directly. Validate changes by loading/reloading the theme in a Home Assistant instance and visually checking both light and dark modes.

HACS requires the theme file to live at `themes/<name>.yaml` at the repo root — don't move it back to the repo root or rename it without updating `hacs.json`.

## Architecture of `themes/vane.yaml`

The theme (`Vane`) is defined in two layers:

1. **Custom color variables** (`vn-*`), defined separately per mode under `modes: dark:` and `modes: light:` — this is where actual color values live (primary colors, backgrounds, text, icons, domain colors like light/cover/climate/media_player, and status colors like error/warning/success/info).
2. **Standard theme keys**, listed flat below the `modes:` block. These map Home Assistant/MDC/paper/bubble-card theme variables (e.g. `primary-color`, `sidebar-background-color`, `mdc-theme-primary`, `bubble-accent-color`) to the `vn-*` variables via `var(--vn-xxx)`. They rarely contain literal color values themselves.

**Implication:** when changing a color, edit the corresponding `vn-*` variable in the `modes:` block (in both `dark` and `light` if needed), not the flat variable list below it — the flat list should stay as indirection through `var(--vn-...)`.

The `version:` field at the end of the file should be bumped when releasing a change, since it's used for HACS-based update tracking.
