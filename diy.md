---
layout: default
---

# DIY projects
{:.no_toc}

* toc  
{:toc}

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

## Idea dump

- dumb ones are easier to do, sample solution: CocoSDC (2 CPLD, 1 FLASH, 1 ATmega MCU)
- a generic solution for the smart ones is to connect it to a PC through USB/RS232/Parallel, (SIO2PC, X1541, ...)

## Resources

- [HXC usb](http://hxc2001.free.fr/floppy_drive_emulator/)
- [CocoSDC](http://cocosdc.blogspot.com.au)
- [ZX Spectrum Beta Disk](http://en.wikipedia.org/wiki/Beta_Disk_Interface)
- [ZX Spectrum divIde](http://baze.au.com/divide/)


# Cartridge emulator

## Resources

- [Z80Teensy](http://labs.domipheus.com/blog/teensy-z80-part-1-intro-memory-serial-io-and-display/)
- [Gameboy cartridge emu with STM32F4](http://dhole.github.io/post/gameboy_cartridge_emu_1/)

# Arcade machine

- [simple one](http://www.instructables.com/id/A-Super-Easy-Arcade-Machine-from-1-Sheet-of-Plywoo/?ALLSTEPS)
 
