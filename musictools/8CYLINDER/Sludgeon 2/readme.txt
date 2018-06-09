 /* Sludgeon2
    by 8CYLINDER
    README Revision date 012.020.2006
    This README pertains to version 2.0 and higher 
    See Sludgeon_README.txt for information on
    earlier versions */

The latest version of Sludgeon2 and this README are always available at: 
http://rhinoplex.org/8cylinder


Summary:
Sludgeon2 is a program that generates melodies on a Gameboy using an Arpeggio-style 
interface.  It can be run on any real Gameboy and/or Gameboy emulator.  Other Gameboy 
sound programs, namely Nanoloop and LSDJ, are excellent, powerful programs.  However, 
both require a great deal of time and button presses just to get any sounds and even more 
time and button presses to make significant pattern and parameter changes.  Sludgeon2 was 
created as a way to quickly generate, play, and modify melodies, particularly for live 
performances.

Sludgeon2 is coded in C and compiled with GBDK.  Source code will be made available after 
the final, fully-tested version of Sludgeon2 is released.


Instructions:
Sludgeon2 can play up to 2 simultaneous patterns of notes in 2 distinct channels, labelled 
A and B.  These channels are controlled by parameters in 3 screens: PTRN (A), PTRN (B), 
and SETTINGS.  All patterns and settings can be saved to and loaded from any of 3 Save
Slots in the SAVE LOAD screen.  Press Start to switch to the next screen and press Select 
to switch to the previous screen.  Press B to start and stop audio.


- PTRN screens (NOTE: the same rules apply to both A and B channels)
The note pattern for each channel is set in that channel's PTRN screen.  Each pattern is 
comprised of up to 8 bars, each up to 8 notes long.  By default, all notes are muted.  
Pressing Left or Right (with no other buttons pressed) causes the Selection Arrow to select 
one of the 8 Note Sliders or the Bar Selector.  If the Selection Arrow is under a Note 
Slider, pressing Up or Down (with no other buttons pressed) causes the value of the Note 
Slider to go up or down.  If the Selection Arrow is under the Bar Selector in the lower
righthand corner, pressing Up or Down cycles through the patterns in the 8 bars of the 
current channel.

>>>> A + Direction controls in PTRN screens
Changing the state and octave of any Note Slider is done by pressing the A button, then 
pressing a direction on the joypad.  With the A button pressed, pressing Up or Down causes
the Octave Dial for that Note Slider to go up or down.  With the A button pressed, 
pressing Left toggles mute on or off, indicated by the square directly beneath the Note 
Slider and immediately above it's Octave Dial (again, all Note Sliders start out muted).  
With the A button pressed, pressing Right toggles the Note Tie on or off, indicated by the
Note Slider changing from a block (Note Tie off) to an arrow (Note Tie on) and vice versa.
Any Notes marked with an 'X' are not played because the time signature has been set to a
value less than 8 (a full Bar).  See time signature below for more information.


- SETTINGS screen
The meta-controls for the A and B channels are managed in the SETTINGS screen:

>>>> TMPO: Beats per minute.
>>>> BARS: The number of bars to play.  Although the user can set the patterns for all 8 
bars for both channels in the BARS screens, this parameter dictates how many bars are 
actually played.  Play starts from bar 1 to whatever this value is set to.  Once the last 
note in this bar is played, the Play Arrow goes back to the beginning of bar 1 and 
continues playing (ie, loops).
>>>> SGN: The time signature.  This dictates how many notes in each bar are played.  When 
set to any value less than 8, any notes in the patterns in the BARS screens above this 
value are marked with an 'X' and are not played.  They can, however, still be edited like 
usual.
>>>> A->: All parameters in the A-> row apply to the A channel.
>>>> B->: All parameters in the B-> row apply to the B channel.

- Channel parameters
>>>> WAVE: Each channel can be set to 1 of 4 different configurations of a square waveform
or 1 of 4 rudimentary pulse width modulations (PWM).  Each PWM cycles through the 4 square
waveforms with different algorithms.
>>>> VLFO: Volume LFO.  Each channel can be made to slowly fade in and out as each bar is 
played.  At 0% (the default) the volume doesn't change.  At 50%, the volume with fade out 
and back in over the course of 4 notes (50% of a bar).  At 100%, the volume with fade out 
and back in over the course of 8 notes (100% of a bar).
>>>> ENV: Envelope.  At FWD, the default, the envelope starts at full volume and drops to 
silence.  At REV, the envelope starts at silence and progresses to full volume.  The REV 
setting vaguely resembles the effect of a record being played backwards.

- Randomizers
The values and states of every Note Slider in both the A and B channels can be randomly set
by pressing the A button when the Selection Arrow is under one of the 3 Randomizer 
parameters.  Once a Randomizer is actuated, there is no way to undo the action:

>>>> NTE: Randomize Notes.  This randomly sets the values of every Note Slider.
>>>> MTE: Randomize Mutes.  This randomly toggles the mute for each Note Slider on or off.
>>>> TIE: Randomize Ties.  This randomly toggles the tie for each Note Slider on or off.

- Additional Notes
Pressing Left and Right causes the Selection Arrow to select a parameter.  Pressing Up or 
Down changes the value of the currently selected parameter.  Normally, values increase or 
decrease by 1.  However, while the TMPO parameter is selected, holding A and pressing Up 
or Down changes the value in increments of 20.


- SAVE LOAD
All patterns and settings can be saved to and loaded from one of 3 Save Slots.  Each row of 
buttons pertains to one Save Slot.  Press Left and Right to move the Selection Arrow under 
a button.  Press the A button when the Selection Arrow is under a SAVE button to save in 
that Save Slot.  Press the A button when the Selection Arrow is under a LOAD button to load
from that Save Slot.  

All patterns and settings are restored to the state store in that Save Slot.  Press the A
button when the Selection Arrow is under a CLR! button to restore all patterns and settings 
in that Save Slot to their original defaults.  This only affects the state of the Save Slot:
the current active patterns and settings are not affected.
