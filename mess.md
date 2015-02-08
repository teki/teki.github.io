---
layout: default
---

# Retro gaming
{:.no_toc}

* toc  
{:toc}

# Quick MESS setup guide

Mini MESS guide: MESS is an emulator which supports a ton of machines.

MESS does not ship with the ROMs/BIOSes of the machines
which it can emulate, they have to be sourced from somewhere else.
MESS has a version number and the ROM packs on the internet has a version number
too. The best is if they match, but it will likely work even if they mismatch.
BIOSes are not enough for emulated computers/consoles, they need software/cartridges
to run. MESS comes with built in lists of software for the systems and sw packages
can be downloaded for the systems.

It is a command line tool, so a UI is recommended to drive it, plus it is a bit tricky to setup. 

- download & install MESS: [mamedev](http://www.mamedev.org/) or [mamedev.emulab](http://mamedev.emulab.it/)
- UI: [qmc2](http://qmc2.arcadehits.net/wordpress/)
- qmc will ask for all sort of paths, point them properly to the installed MESS's directories (IMPORTANT!, do as many as you can)
- bios package: google is your friend, search for "mame bios rom collection", there are a few on archive.org too, unzip this to the rom directory of MESS
- now you need software for the emulated system, google for: "MESS Software List ROMs", archive.org is your friend again
- uncompress this sw package into the hash folder of the installed MESS (it will create a subdirectory inside it, with the name of the system, and the programs wibb be inside that)
- then in qmc2 choose the machine in the left side, select the software list tab on the right side and double click starts the action!

MESS will not work if the paths are no set up properly. ROMs/BIOSes are meant to
be in the rom directory, softwares must be in the hash directory in a subdirectory
which corresponds to the emulated system. Plus qmc2 has to have all the correct
paths to these directories. There is a log in the bottom right of qmc2, but it only
will tell you that something was not found, check the paths again and again and again.

# Good Games

Good source of games to try: [The Video Game Critic](http://videogamecritic.com/)
It is possible to order them by rating, like: [Colecovision](http://videogamecritic.com/coleco_g.htm)
Most game's manual can be found on archive.org.

Games I liked:

## Colecovision

- Frenzy - Berzerk sequel, running around in a labirynth shooting robots, tip: shooting is tricky, press fire first then use the joystick/direction pad to aim
- Dragonfire - muscle memory fun, very fast, repeptitive