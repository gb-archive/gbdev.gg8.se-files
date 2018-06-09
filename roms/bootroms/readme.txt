This is a collection of all known boot ROMs dumped from various Gameboy models.
These is the code that is responsible for displaying the scrolling Nintendo
logo on startup, playing the iconic po-ling sound, as well as verifying the
logo and header checksum in an attempt to lock out unlicensed cartridges.

They can be used in supported emulators to emulate the full boot process.

Normally, these ROMs are disabled when control is handed over to the game
cartridge, which makes dumping them difficult, but various methods have been
devised throughout the years to make dumping them possible.

The bootstraps are discussed further on the following GB Dev Wiki page:

http://gbdev.gg8.se/wiki/articles/Gameboy_Bootstrap_ROM

File list
=========
dmg_rom.bin         - The DMG boot ROM.
This is the most common version of the boot ROM found in the original DMG-01
model of Gameboy. 

dmg0_rom.bin        - Early DMG boot ROM with different behavior.
This is the very early variant of the DMG boot ROM which is only found in very
early Japan-sold DMG units. It has a different behavior in that it makes the
screen flash if the boot process fails, instead of scrolling down a 
(potentially corrupted looking) logo and hanging.

mgb_boot.bin        - The Pocket Gameboy boot ROM.
Only differs from dmg_rom.bin in one byte, which loads the value $FF into the
A register instead $01 just before handing over the control to the game. This
can be used by the game to detect that it is running on MGB hardware.

sgb_boot.bin        - The Super Gameboy boot ROM.
Instead of showing a logo animation, this ROM sends the ROM header to the SNES
part of the Super Gameboy, which shows a fancy animation before displaying the
Gameboy screen.

sgb2_boot.bin       - The Super Gameboy 2 boot ROM.
Aanalogous to mgb_boot.bin, the SGB2 boot ROM only differs from the SGB boot
ROM in one byte loading a value into the A register which allows SGB2 hardware
to be distinguished from SGB hardware.

gbc_bios.bin        - The Gameboy Color boot ROM
The GBC boot ROM is spread out over a bigger memory area than the original 256
bytes, and has slightly increased functionality compared previous boot ROMs,
including the ability to choose a palette from a number of presets for non-GBC
enabled games.

gamefighter_rom.bin - Boot ROM from the Gameboy clone Game Fighter.
fortune_rom.bin     - Boot ROM from the Gameboy clone Fortune/Bitman 3000B.
These boot ROMs are dumped from two unlicensed Gameboy clones which each has a
rather different boot ROM compared to the originals.

Using these files with emulators
================================
* BGB
BGB has support for boot ROMs, which can be enabled by going to the system tab
in the settings, entering a path to the ROM in question, and checking "bootroms
enabled".

* Higan
Higan needs the SGB and/or SGB2 boot ROM for correctly running Super Gameboy
enhanced software. The SGB boot ROM in particular can't be emulated through HLE
(high level emulation) since it communicates with the SNES. Using these files
with Higan is documented here:

https://higan.readthedocs.io/en/stable/guides/import/#super-game-boy-games

* Mooneye-GB
Mooneye-GB, an accuracy focused Gameboy emulator written by gekkio (the same
person mentioned in the history section) supports boot ROMs and in fact 
requires them to guarantee cycle accurate emulation.

History
=======
The first time anyone published a dump of such a ROM was in 2003 when neviksti
decapped a DMG CPU and manually read out each individual bit, all 2048 of them.

https://dot-matrix-game.blogspot.com/2014/01/boot-roms.html
http://www.neviksti.com/DMG/

In 2009, the Super Gameboy and Gameboy Color boot ROMs were dumped by Costis
Sideris. The SGB boot ROM was dumped using an overclock attack, whereas the GBC
boot ROM was dumped using a power and clock glitch attack.

https://www.its.caltech.edu/~costis/sgb_hack/

In 2014, BennVenn came up with a simple clock glitching method which requires
nothing but a piece of wire. The method consists of connecting one side of the
crystal oscillator circuit to ground briefly, which makes the CPU jump to a
random place in memory without disabling the boot ROM, which allows it to be
read out. By using this method, he was able to dump the MGB (Gameboy Pocket)
boot ROM.

https://web.archive.org/web/20151014210143/http%3A//www.bennvenn.com/MGB.htm

The same year nitro2k01 (the person running this site and writing this text)
dumped the boot ROM of two unlicensed Gameboy clones using BennVenn's method.
They have a slightly different behavior from the original ones and may be
partially or fully rewritten.

http://blog.gg8.se/wordpress/2014/12/09/dumping-the-boot-rom-of-the-gameboy-clone-game-fighter/

In 2015 gekkio, using another overclock attack, dumped the SGB2 boot ROM.

https://gekkio.fi/blog/2015-09-13-dumping-the-super-game-boy-2-boot-rom.html

In 2016, gekkio also dumped an variant of the DMG boot ROM only found in very
early DMG units, now dubbed dmg0 in the world of Gameboy research.

https://gekkio.fi/blog/2016-10-04-game-boy-research-status.html

The only known variant that has not yet been dumped is the GBA version of the
GBC boot ROM. Just like the MGB and SGB2 variants, the only change in the GBA
version of the GBC boot ROM seems to be that the CPU B register has a different
value to allow detection of GBA hardware. 

File hashes
===========
SHA256:
26e71cf01e301e5dc40e987cd2ecbf6d0276245890ac829db2a25323da86818e  dmg0_rom.bin
cf053eccb4ccafff9e67339d4e78e98dce7d1ed59be819d2a1ba2232c6fce1c7  dmg_boot.bin
9e328227920e86d5530f54efedb562e9ce5b6d32a4ecdee0a278a3d9c6a114b1  fortune_rom.bin
7abdaeea7ac2afd39d86a2ddf044fb978ccd4e65fa4ef15ffc8fcd19df71f254  gamefighter_rom.bin
b4f2e416a35eef52cba161b159c7c8523a92594facb924b3ede0d722867c50c7  gbc_bios.bin
a8cb5f4f1f16f2573ed2ecd8daedb9c5d1dd2c30a481f9b179b5d725d95eafe2  mgb_boot.bin
fd243c4fb27008986316ce3df29e9cfbcdc0cd52704970555a8bb76edbec3988  sgb2_boot.bin
0e4ddff32fc9d1eeaae812a157dd246459b00c9e14f2f61751f661f32361e360  sgb_boot.bin


SHA1:

8bd501e31921e9601788316dbd3ce9833a97bcbc  dmg0_rom.bin
4ed31ec6b0b175bb109c0eb5fd3d193da823339f  dmg_boot.bin
f9d63ac153c378145fe04c052951ad5cf12ac916  fortune_rom.bin
a4a36f71bf1b3b587df620d48ae940af93a982a5  gamefighter_rom.bin
1293d68bf9643bc4f36954c1e80e38f39864528d  gbc_bios.bin
4e68f9da03c310e84c523654b9026e51f26ce7f0  mgb_boot.bin
93407ea10d2f30ab96a314d8eca44fe160aea734  sgb2_boot.bin
aa2f50a77dfb4823da96ba99309085a3c6278515  sgb_boot.bin

MD5:

a8f84a0ac44da5d3f0ee19f9cea80a8c  dmg0_rom.bin
32fbbd84168d3482956eb3c5051637f5  dmg_boot.bin
92ed4eca17d61fcd53f8a64c3ce84743  fortune_rom.bin
6a7b8ee12a793f66a969c6a2b8926cc9  gamefighter_rom.bin
dbfce9db9deaa2567f6a84fde55f9680  gbc_bios.bin
71a378e71ff30b2d8a1f02bf5c7896aa  mgb_boot.bin
e0430bca9925fb9882148fd2dc2418c1  sgb2_boot.bin
d574d4f9c12f305074798f54c091a8b4  sgb_boot.bin
