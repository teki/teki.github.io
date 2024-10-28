---
layout: page
---

# DIY projects

# Floppy disk emulator

## Smart floppies (serial communication)

- Atari
  - Atar 810: 6507 CPU + WD1771 [schematics](http://www.dereatari.republika.pl/literat/810fsm.pdf)
  - Atari 1050: 6507 CPU + WD273 [schematics](https://nuxx.net/gallery/v/computers/atari800xl/atari1050_schematic.png.html?g2_imageViewsIndex=2)
- Commodore
  - 1541: 6502 CPU + custom hw [schematics](http://www.zimmers.net/anonftp/pub/cbm/schematics/drives/new/1541/1541-II.gif)

## Dumb floppies

- TRS-80 Color Computer:
  - Card1: WD1773 [schematics](http://www.colorcomputerarchive.com/coco/Documents/Manuals/Hardware/Western%20Digital%20Floppy%20Controller%20-%20WD1773%20Schematic%20Diagram.gif)
  - Card2: WD1793 [schematics](http://www.colorcomputerarchive.com/coco/Documents/Manuals/Hardware/Western%20Digital%20Floppy%20Controller%20-%20WD1793%205V%20Schematic%20Diagram.gif)
- Videoton TVC
  - HBF-2: WD1793 [schematics](http://tvc.homeserver.hu/doc/tervrajzok/hba2/tvc_floppy_2005.png)
- ZX Spectrum
  - Beta Disk: WD1793
- Amstrad CPC
  - DDI-1: R6765 [schematics](http://www.cpcwiki.eu/imgs/4/4f/DDI_Schematic.png)

## Non standard floppies (custom rom involved)

- ZX Spectrum
  - [CF and IDE connection](http://piters.tripod.com/zx.htm) [CF card howto](https://www.sparkfun.com/datasheets/BreakoutBoards/c0201mspdf.pdf)

## Idea dump

- dumb ones are easier to do, sample solution: CocoSDC (2 CPLD, 1 FLASH, 1 ATmega MCU)
- a generic solution for the smart ones is to connect it to a PC through USB/RS232/Parallel, (SIO2PC, X1541, ...)

## Resources

- [HXC usb](http://hxc2001.free.fr/floppy_drive_emulator/)
- [CocoSDC](http://cocosdc.blogspot.com.au)
- [ZX Spectrum Beta Disk](http://en.wikipedia.org/wiki/Beta_Disk_Interface)
- [ZX Spectrum divIde](http://baze.au.com/divide/)

# STM32F4 OSX toolchain

- [homebrew](http://brew.sh)
- [compiler](https://launchpad.net/gcc-arm-embedded/)
- [debugger 1](http://openocd.sourceforge.net) homebrew: brew install open-ocd
- [debugger 2](https://github.com/texane/stlink) homebrew: brew install stlink
- [IDE installation guide](http://grafixmafia.net/updated-using-the-stm32f4-discovery-board-with-mac-osx-10-9-mavericks/)
  - install [eclipse c/c++](https://www.eclipse.org/downloads/)
  - install all gnuarm plugins: http://gnuarmeclipse.sourceforge.net/updates
  - install "GCC Cross Compiler support" and "GDB Hardware Debugging" from: http://download.eclipse.org/tools/cdt/releases/kepler
  - new C project will have an option for "STM32F4XX C/C++ Project", defaults are mostly ok, you have to point to the arm toolchain in the last step!
- integrate a debugger provider (optional):
  - add new external program (green play icon with red toolbox)
  - Location: /usr/local/bin/st-util
  - Working Directory: ${project_loc}
  - this will just run that tool, you can do it on the command line, it will print the default port for the gdb server
- integrate debugger
  - Debug Configurations (under Run menu)
  - new
  - on the Debugger tab set the path to gdb in the arm toolchain
  - JTAG device: generic tcp
  - port: 4242 (default for stlink)

# Cartridge emulator

## Resources

- [Z80Teensy](http://labs.domipheus.com/blog/teensy-z80-part-1-intro-memory-serial-io-and-display/)
- [Gameboy cartridge emu with STM32F4](http://dhole.github.io/post/gameboy_cartridge_emu_1/)

# Arcade machine

- [simple one](http://www.instructables.com/id/A-Super-Easy-Arcade-Machine-from-1-Sheet-of-Plywoo/?ALLSTEPS)

# iMac HDD upgrade (without opening it)

- Kanex Thunderbolt-to-Gigabit Ethernet + USB 3.0 Adapter (Apple store) $110
- OWC Mercury Elite Pro Mini USB3 35USD - 100AUD
- SSD

# C64 cartridge based on Magic Desk I

- [mod](http://users.on.net/~clockmeister/other/EPROM-Cartridge/Magic-Desk-4x8k-mod/)
- parts: 4* 2764 eproms + sockets28, dip 4 switch, 2* sockets16, reset button

# Amstrad RGB cable

- [a simple one](http://www.cpcwiki.eu/index.php/TV_SCART_cable)
- parts: scart plug, stereo jack, 100uF (optional), 6 pin DIN plug
- [scart pins](http://www.leadsdirect.co.uk/technical-library/pinouts-wiring-diagrams/scart-wiring/)

# ZX Spectrum +2 RGB cable

- [pdf](http://mts.speccy.cz/doc/128_rgb.pdf)

# Amstrad CPC tape drive replacement

- [size: 74mm x 1.2mm](http://www.cpcwiki.eu/forum/amstrad-cpc-hardware/repair-a-cpc-464-cassette-tape-deck/)

# Atari USB2SIO

- parts: serial to usb board (CH340G, ~1$), USB socket
