 /* UCBN 1.001
    by 8CYLINDER
    README Revision date 009.002.2004 */

The final version of UCBN and this README are always available at:
http://rhinoplex.org/8cylinder


Summary:
The User-Constrained Brownian Noise generator (UCBN) is a very simple program that plays 
brownian noise based on parameters set by the user. It can be run on any real Gameboy 
and/or Gameboy emulator.  UCBN can also generate white noise.  Version 1.001 is the final 
version: there will not be any further development on this program.

UCBN was coded in C and compiled with GBDK.


Instructions:
Noise begins as soon as UCBN starts.  Noise is created by playing a tone at a random 
frequency and after a certain amount of time, the tone may change to another random 
frequency according to the user-constrained parameters.  The parameters the user can set 
are:

- FREQLEVEL: frequency level.  This parameter dictates the general range of frequencies 
that the generator will traverse.
- DISTRIB: distribution.  Sets the tendancy towards raising or lowering the frequency when 
the frequency changes.  If set in the middle, there is equal change next tone will raised 
or lowered.  As the tone reaches the edge of the range of legal fequencies, however, this
parameter is likely to be overridden.
- VARIATION: variation.  Determines the maximum difference in value the next 
frequency may be from the current frequency.
- TONELEN: tone length.  This parameter sets the amount of time a frequency will play 
before changing to the next frequency.
- BROWNIAN: toggles brownian random routines on and off. If off, the currently playing 
frequency will not change.
- WHITE: toggles white noise on and off.
