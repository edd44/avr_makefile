avr_makefile
============

Quite universal makefile for AVR MCUs projects.

## Prerequisites
To run this makefile avr-gcc, avr-libc, avrdude and avrdoper are need.
If you're on Ubuntu, just run
	$ sudo apt-get install gcc-avr avrdude

## Usage
1. Set proper project specific and programmer settings on Makefile
2. Add necessary libraries in Makefile
3. Test connection between PC and MCU]
	$ sudo make test_connection
4. Run building (may be ommited)
	$ make build
5. Upload hex to MCU
	$ sudo make run

To list all make targets:
	$ make
		and press TAB key

	