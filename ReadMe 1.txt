Features
Detects and initializes the WUP-028 adapter.
Reads inputs from up to 4 GameCube controllers (buttons, D-pad, analog sticks).
Logs controller inputs to wiiu_gcn_sdl2.log.
Basic SDL2 window for testing.

Prerequisites
Libraries:
SDL2 (libsdl2-dev on Linux, or equivalent on Windows via MSYS2).
libusb-1.0 (libusb-1.0-0-dev on Linux, or compiled manually on Windows).
Driver (Windows):
Install WinUSB driver for WUP-028 using Zadig.
Adapter:
Ensure the adapter is in Wii U mode (for Mayflash adapters, check the physical switch).