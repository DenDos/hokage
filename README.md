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
2. Install dependencies:

```bash
brew install qmk/qmk/qmk avr-gcc
```

### Setup

```bash
cd ~/qmk_firmware

# This keymap requires QMK 0.11.50
git checkout 0.11.50

# Clone this repo into the Corne keymaps folder
cd keyboards/crkbd/keymaps
git clone https://github.com/DenDos/hokage.git
```

### Build & Flash

> **Important:** The Homebrew `qmk` CLI (v1.1.6+) is incompatible with QMK firmware 0.11.50.
> Use `make` instead of the `qmk` command.

```bash
cd ~/qmk_firmware

# Compile
make crkbd:hokage

# Flash (repeat for each half)
make crkbd:hokage:avrdude
```

The flash command will print `Detecting USB port, reset your controller now...`
and wait for the keyboard to enter bootloader mode.

### Flashing procedure (both halves)

1. Connect the **left half** via USB
2. Run `make crkbd:hokage:avrdude`
3. Enter bootloader mode (see below)
4. Wait for flash to complete and verify
5. Disconnect left, connect **right half** via USB
6. Repeat steps 2-4

### Entering bootloader mode (software reset)

No physical reset button needed. The RESET key is on **Layer 3 (ADJUST)**,
top-left position (where TAB normally is):

1. Hold **LWR** (left thumb middle) + **RSE** (right thumb middle) simultaneously
2. While holding both, tap the **top-left key** (TAB position)

> The Pro Micro bootloader only stays active for ~8 seconds.
> Start the `make crkbd:hokage:avrdude` command **before** pressing RESET
> so it detects the device automatically.

After flashing both halves, connect only the **left half** (master) to your Mac.
The right half communicates over the TRRS/serial cable.

---

## Troubleshooting

### `qmk compile` fails with `conflicting subparser: config`

The Homebrew `qmk` CLI is too new for QMK 0.11.50. Use `make` instead:

```bash
make crkbd:hokage          # compile
make crkbd:hokage:avrdude  # flash
```

### `avrdude` config errors (`unknown token`, `syntax error`)

If `avrdude` was upgraded to v8.x, its config file at `/opt/homebrew/etc/avrdude.conf`
may be corrupted or incompatible. Fix by replacing it with the correct version
from the Homebrew bottle:

```bash
cp /opt/homebrew/Cellar/avrdude/$(avrdude 2>&1 | grep -oP '[\d.]+')/\
.bottle/etc/avrdude.conf /opt/homebrew/etc/avrdude.conf
```

Or reinstall: `brew reinstall avrdude`

### Bootloader times out before flash starts

The Pro Micro bootloader is only active for ~8 seconds. Always start the
flash command first, then press the reset combo while it's waiting.

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
