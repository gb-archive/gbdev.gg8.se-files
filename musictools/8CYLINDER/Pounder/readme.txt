 /* Pounder 2.0
    by 8CYLINDER
    README Revision date 009.002.2004 */

The latest version of Pounder and this README are always available at:
http://rhinoplex.org/8cylinder


Summary:
Pounder is a very simple program that plays drum samples when the corresponding button or 
joystick press is made.  It can be run on any real Gameboy and/or Gameboy emulator.  
Initially, a text-only version of Pounder was used to test the samples that were being 
imported into ShitTracker.  Because of this, Pounder includes the same drum kits as 
Shittracker.

Pounder is coded in C and compiled with GBDK.  Source code will be made available after 
the final, fully-tested version of Pounder is released.


Instructions:
Pounder is comprised of one screen.  Pressing Up (High Hat), Down (Crash Cymbol), 
Left (Snare Drum 1), Right (Snare Drum 2), A (909 Bass Drum 1), B (909 Bass Drum 2), 
Left+A (Low Tom), and Right+B (High Tom) triggers the corresponding percussion sample.  
Pressing Select switches between the 5 banks/drum kits, labelled A through E.  Pressing 
Start cycles through the delay settings.  At 0 delay, there is no delay after a sample is 
played and the next sample is triggered immediately afterwards while any trigger button is 
pressed.  Besides the implications this lack of delay has when a button is held down for 
long periods of time, 0 delay can also cause incidental "double time" triggers when the 
user presses a button once, but does not release the button within the 0.25 seconds it 
takes for a sample to play.  By moving to the 1-5 delay settings, this "double time" 
trigger effect becomes less likely to occur.
