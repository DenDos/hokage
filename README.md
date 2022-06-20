# Cotoha's layout for Corne

Features:

* Modern OLED support (many thanks to @drashna):
  * Proper orientation
  * Graphic layer indicator ↑ ↓
  * Graphic modifier indicator ⌘ ⇧ ⌥  ⌃
* Similar enough to the default keymap so you can easily port your custom keymap to it
* Mac-friendly (Command and Option on the thumbs)
* Vim-friendly (Esc, `:` and Ctrl on the thumbs)
* Full per-key RGB Matrix support out of the box (you still have to go through the nightmare of soldering yourself though 😉)


## Installation

```bash
  # first follow these steps 
  # https://docs.qmk.fm/#/newbs_getting_started
  
  # then go to qmk_firmware folder
  cd /Users/#{your_user_name}/qmk_firmware
  
  # Current firmware works only for qmk_firmware 0.11.50
  git checkout 0.11.50

  # Go to keymaps folder
  cd /keyboards/crkbd/keymaps
  
  # Clone the hokage repo
  git clone https://github.com/DenDos/hokage.git
  
  # make sure you have avr-gcc installed
  brew install avr-gcc
  
  # Compile firmware
  qmk compile -kb crkbd -km hokage
  
  # Flash it 🚀
  qmk flash -kb crkbd -km hokage

```
