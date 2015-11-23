avr_makefile
============

Quite universal makefile for AVR MCUs projects.

## Prerequisites
To run this makefile avr-gcc, avr-libc, avrdude and avrdoper are need.
If you're on Ubuntu, just run `sudo apt-get install gcc-avr avrdude`

## Usage
1. Set proper project specific and programmer settings on Makefile
2. Add necessary libraries in Makefile
3. Test connection between PC and MCU `sudo make test_connection`
4. Run building `make build` (may be ommited)
5. Upload hex to MCU `sudo make run`

To list all make targets `make` and press TAB key.

## Linking with project
1. In project root directory run `git submodule add https://github.com/edd44/avr_makefile.git ./make/`
2. Create a link to Makefile `ln make/Makefile Makefile -s`
3. To update git submodules run `git submodule foreach git pull`

## Running without root permissions
1. `echo 'SUBSYSTEM=="usb", ENV{DEVTYPE}=="usb_device", MODE="0664", GROUP="dialout"' | sudo tee /etc/udev/rules.d/30-usb-devices.rules >/dev/null`
2. `sudo adduser ${USERNAME} dialout`
