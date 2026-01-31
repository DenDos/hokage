# Hokage - Corne Keyboard Layout

Custom QMK keymap for the **Corne (crkbd)** split ergonomic keyboard (42 keys).

## Features

- **Mac-friendly**: Command and Option on the thumbs
- **Vim-friendly**: Esc, `:` and Ctrl on the thumbs
- **OLED displays**: 128x64 SSD1306 with layer/modifier indicators (270° rotation)
- **Per-key RGB Matrix**: WS2812 with typing heatmap, solid reactive effects
- **NKRO**: Full N-Key Rollover support

---

## Current Layout

### Layer 0: QWERTY (Default)

```
        ЛЕВАЯ РУКА                              ПРАВАЯ РУКА
╭──────┬─────┬─────┬─────┬─────┬─────╮   ╭─────┬─────┬─────┬─────┬─────┬──────╮
│ TAB  │  Q  │  W  │  E  │  R  │  T  │   │  Y  │  U  │  I  │  O  │  P  │  [   │
├──────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼──────┤
│ SHIFT│  A  │  S  │  D  │  F  │  G  │   │  H  │  J  │  K  │  L  │  ;  │  '   │
├──────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼──────┤
│ CTRL │  Z  │  X  │  C  │  V  │  B  │   │  N  │  M  │  ,  │  .  │  /  │  ~   │
╰──────┴─────┴─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┴─────┴──────╯
                    │ CMD │LWR ⬇│ SPC │   │ ENT │RSE ⬆│ ALT │
                    ╰─────┴─────┴─────╯   ╰─────┴─────┴─────╯
                      👈 большие пальцы 👉
```

**Thumb keys (большие пальцы):**

| Клавиша | Рука | Палец | Действие |
|---------|------|-------|----------|
| CMD | Левая | Большой | Command (macOS) |
| LWR | Левая | Большой | Зажать → Layer 1 (цифры, стрелки) |
| SPC | Левая | Большой | Пробел |
| ENT | Правая | Большой | Enter |
| RSE | Правая | Большой | Зажать → Layer 2 (символы, F-клавиши) |
| ALT | Правая | Большой | Option (macOS) |

### Layer 1: LOWER (Numbers & Navigation)

> Зажми **LWR** — **левая рука**, большой палец, средняя клавиша.

```
╭──────┬─────┬─────┬─────┬─────┬─────╮   ╭─────┬─────┬─────┬─────┬─────┬──────╮
│ ESC  │  1  │  2  │  3  │  4  │  5  │   │  6  │  7  │  8  │  9  │  0  │      │
├──────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼──────┤
│ SHIFT│     │     │     │     │     │   │  ←  │  ↓  │  ↑  │  →  │     │      │
├──────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼──────┤
│ CTRL │     │     │     │     │     │   │ BSPC│     │     │     │     │      │
╰──────┴─────┴─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┴─────┴──────╯
                    │ CMD │ ▓▓▓ │ SPC │   │ ENT │ADJ  │ ALT │
                    ╰─────┴─────┴─────╯   ╰─────┴─────┴─────╯
```

### Layer 2: RAISE (Symbols & F-keys)

> Зажми **RSE** — **правая рука**, большой палец, средняя клавиша.

```
╭──────┬─────┬─────┬─────┬─────┬─────╮   ╭─────┬─────┬─────┬─────┬─────┬──────╮
│ ESC  │  !  │  @  │  #  │  $  │  %  │   │  ^  │  &  │  *  │  (  │  )  │ BSPC │
├──────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼──────┤
│ SHIFT│ F1  │ F2  │ F10 │ F11 │ F12 │   │  -  │  =  │  {  │  }  │  |  │  `   │
├──────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼──────┤
│ CTRL │ F7  │ F8  │ F9  │HOME │ END │   │  _  │  +  │  [  │  ]  │  \  │  ¬   │
╰──────┴─────┴─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┴─────┴──────╯
                    │ CMD │ADJ  │ SPC │   │ ENT │ ▓▓▓ │ ALT │
                    ╰─────┴─────┴─────╯   ╰─────┴─────┴─────╯
```

### Layer 3: ADJUST (RGB & System)

> Зажми **LWR + RSE** одновременно — **оба больших пальца**, средние клавиши на обеих руках.

```
╭──────┬─────┬─────┬─────┬─────┬─────╮   ╭─────┬─────┬─────┬─────┬─────┬──────╮
│RESET │     │     │     │     │RGBRS│   │     │     │     │     │     │      │
├──────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼──────┤
│RGBTOG│ HUE+│ SAT+│ VAL+│     │     │   │     │     │     │     │     │      │
├──────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼──────┤
│RGBMOD│ HUE-│ SAT-│ VAL-│     │     │   │ BSPC│     │     │     │     │      │
╰──────┴─────┴─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┴─────┴──────╯
                    │ CMD │ ▓▓▓ │ SPC │   │ ENT │ ▓▓▓ │ ALT │
                    ╰─────┴─────┴─────╯   ╰─────┴─────┴─────╯
```

> `▓▓▓` = transparent (passes through to layer below)

---

## File Structure

| File | Description |
|------|-------------|
| `keymap.c` | Keymap layers, OLED rendering, custom key processing |
| `config.h` | QMK config: tapping term (150ms), RGB, OLED, serial settings |
| `rules.mk` | Build features: RGB_MATRIX, OLED, NKRO |
| `rgb.c` | Per-layer RGB color logic |
| `glcdfont.c` | Custom OLED font with layer/modifier indicator glyphs |

---

## Installation

### Prerequisites

1. Install QMK toolchain following the [official guide](https://docs.qmk.fm/#/newbs_getting_started)
2. Make sure `avr-gcc` is installed:

```bash
brew install avr-gcc
```

### Setup

```bash
# Go to your qmk_firmware directory
cd ~/qmk_firmware

# This keymap requires QMK 0.11.50
git checkout 0.11.50

# Clone this repo into the Corne keymaps folder
cd keyboards/crkbd/keymaps
git clone https://github.com/DenDos/hokage.git
```

### Build & Flash

```bash
# Compile the firmware
qmk compile -kb crkbd -km hokage

# Flash to keyboard (put keyboard in bootloader mode first)
qmk flash -kb crkbd -km hokage
```

> Repeat the flash command for each half of the keyboard.

---

## Customization

- **Tapping term**: Change `TAPPING_TERM` in `config.h` (default: 150ms)
- **RGB effects**: Enable/disable animations in `config.h` (`#define`/`#undef`)
- **OLED font**: Edit `glcdfont.c` using [Helix Font Editor](https://helixfonteditor.netlify.com/)
- **Keymap**: Modify layer arrays in `keymap.c`

## Hardware

- **Keyboard**: Corne (crkbd) — 42-key split
- **Master half**: Left
- **Displays**: SSD1306 128x64 OLED (rotated 270°)
- **LEDs**: WS2812 per-key RGB
- **Communication**: Serial (PD2 pin)
