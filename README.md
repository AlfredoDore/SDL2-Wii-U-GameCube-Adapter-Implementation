# SDL2-Wii-U-GameCube-Adapter-Implementation
This project is an SDL2-based implementation for the Nintendo Wii U GameCube Controller Adapter (WUP-028), inspired by the pj64-wiiu-gcn plugin for Project64. It uses libusb to communicate with the adapter and SDL2 for basic event handling, allowing GameCube controller inputs to be read on Windows and Linux.

1 - git clone https://github.com/seu-usuario/sdl2-wiiu-gcn-adapter.git
cd sdl2-wiiu-gcn-adapter

2 Install dependencies

Linux:sudo apt-get install libsdl2-dev libusb-1.0-0-dev

Windows (MSYS2 MINGW32): Install SDL2 via pacman -S mingw-w64-i686-SDL2. For libusb, follow these instructions: git clone https://github.com/libusb/libusb
cd libusb
./bootstrap.sh && ./configure && make -j && make install

3 Compile the code:

Linux: gcc wiiu_gcn_sdl2.c -o wiiu_gcn_sdl2 -lSDL2 -lusb-1.0 -I/usr/include/libusb-1.0
Windows (MSYS2): gcc wiiu_gcn_sdl2.c -o wiiu_gcn_sdl2 -lSDL2 -l:libusb-1.0.a -static-libgcc

4 - Run the program:
./wiiu_gcn_sdl2

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
