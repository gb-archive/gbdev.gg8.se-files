Pushpin modded for Arduinoboy/nanoloop MIDI
===========================================
This is a version of Pushpin which has been modded to use the regular link port
protocol instead of Pushpin's original hack of reading MIDI UART directly on a
digital IO pin on the GBC link port. This version works with Arduinoboy in mGB
mode or the nanoloop MIDI adapter in MIDI mode. This version no longer works
with Pushpin's original MIDI UART mode.

It has been modified to be able to run on non-GBC Gameboys, since Pushpin hangs
when it tries to switch to GBC double speed mode. The display is slightly
glitched on monochrome Gameboy but otherwise it should work fine.

This version works just like the original. Press up/down to select MIDI channel
assignment, then press start to begin receiving MIDI. Refer to Pushpin's manual
for advanced usage and MIDI CC assignment.

Since I don't have a GBDK environment set up, it was easier for me to do this
by modifying the ROM using BGB. For this reason there's currently no source 
code. I should probably make a proper release source code at some point. Such
a version could offer a mode selection at boot time to allow either MIDI UART
mode or SPI mode.

nitro2k01 - 2016-11-14 
http://blog.gg8.se/wordpress/

Pushpin documentation and source code:
https://github.com/bwhitman/pushpin
