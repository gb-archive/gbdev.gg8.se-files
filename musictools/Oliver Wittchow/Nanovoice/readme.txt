nanovoice
4-bit lofi synth
Nanovoice is a primitive additive synthesizer for the old Game Boy types (DMG).  Within a repeatedly playing spectral matrix of 16 time slots and 16 harmonic frequencies, the volume for each pixel can be set in 4 steps. The base/sampling frequency is variable, but only in a very raw resolution which does not match any musical scale.

 

Sets can be saved in 15 memory slots. Saving stops sound for a second.

Nanovoice does not play Game Boy specific sounds with the console's built-in synth functions but implements its own synthesis scheme while the soundchip is misused as D/A converter. Digital audio output is realized via amplitude modulation of the Game Boy's two rectangular wave generators, resulting in a 4-bit stereo audio stream with a variable sampling frequency below 4 kHz.

Nanovoice was developed just to demo the possibility of sampled audio playback in stereo on an oldschool dot matrix Game Boy. It lacks any advanced editing features and could, unlike nanoloop, hardly serve as standalone tool for music creation. It may, however, be used in combination with other sound sources (can sync timing with nanoloop via link cable or midi devices via midi sync cable) to add some dirty 4-bit flavour to your setup. Furthermore it can generate nice, smooth bass pads when played through a lowpass filter.


Before purchasing nanovoice on a cart, it is highly recommended to try it in an emulator, otherwise you may be disappointed with the limited functionality. Nanovoice sounds best on the original Game Boy (DMG), but also works on Game Boy Pocket, Game Boy Advance and GBA SP. It does not run on Game Boy Color, GB micro and DS.


The concept of spectral / additive synthesis is rather common and used in many synthesizers. A simple and nice example is "javoice", which was the original model for nanovoice (and its name as well, obviously):




nanovoice instructions


B: turn pixel on 
A: mute pixel 

B+up/down: set volume 
B+left/right: switch pixel to noise/sine mode 

START+up/down: change sampling frequency 
START+left/right: change tempo 
START+A/B: external sync on/off 
SELECT: toggle file menu 

in file menu: 

B+up/down: load / save
left/right: select file slot 
A+B+up: clear pattern 

on flashcarts and emulators only one file slot is available, writing to / reading from any slot will access slot 0.
