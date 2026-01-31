# Hokage - QMK Keymap for Corne (crkbd)

## Project Overview

Custom QMK firmware keymap for the Corne (crkbd) split ergonomic keyboard (42 keys).
Optimized for macOS and Vim workflows.

## File Structure

| File | Purpose |
|------|---------|
| `keymap.c` | Main keymap: layer definitions, OLED rendering, key processing |
| `config.h` | QMK configuration: tapping term, RGB settings, OLED, serial |
| `rules.mk` | Build rules: enabled features (RGB_MATRIX, OLED, NKRO) |
| `rgb.c` | RGB per-layer color logic (currently commented out) |
| `glcdfont.c` | Custom OLED font with layer/modifier indicator graphics |
| `README.md` | User-facing documentation with layout diagrams |

## Layers

- `_QWERTY` (0) - Default QWERTY layout
- `_LOWER` (1) - Numbers, arrow navigation, Backspace
- `_RAISE` (2) - Symbols, F-keys, Home/End, brackets
- `_ADJUST` (3) - RGB controls, firmware RESET (activated by Lower+Raise)

## Key Conventions

- Thumbs: CMD (left), Layer toggle (center), Space/Enter (inner), ALT (right)
- Modifiers on home row left: Shift, Ctrl
- `KC_LGESC` = GUI/Escape dual-function
- `KC_RACL` = Right Alt / `:` on tap (Vim-friendly)

## Build Requirements

- QMK Firmware version **0.11.50**
- `avr-gcc` toolchain
- Master half: LEFT
