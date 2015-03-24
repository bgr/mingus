#summary Tips on setting up mingus
#sidebar mingusSidebar


---


# Setup #

## Installing from Source ##

  1. Get the `tar.gz` archive.
  1. Unpack
  1. Open a terminal or 'prompt' and `cd` to the directory to which you unpacked.
  1. Type `python setup.py install`

## Installing .deb or Windows Package ##

  1. Get the `deb` or `exe` installer.
  1. Run it.

## Installing from your default package manager ##

mingus might be packaged for your distribution's package manager. See [getting mingus](tutorialGettingmingus.md) for a list.


## Recommended Programs ##

  1. You may also want to install LilyPond to generate sheet music: http://www.lilypond.org/
  1. Additionally, you can install FluidSynth for realtime MIDI playback support: http://fluidsynth.resonance.org/trac

### Installing FluidSynth on Windows ###

Installing FluidSynth on Linux and Mac shouldn't be a problem, doing it on Windows is a little bit more complex:

  1. Download and install QSynth (http://qsynth.sourceforge.net) which contains a patched version of FluidSynth which works on Windows.
  1. Add the QSynth directory to your PATH.
  1. In the QSynth directory, copy libfluidsynth-1.dll to libfluidsynth.dll


---


  * [Back to Index](mingusIndex.md)