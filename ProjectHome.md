# mingus #

## What's mingus? ##

### Intervals, Chords, Scales and Progressions ###

mingus is a package for Python used by programmers, musicians, composers and researchers to make and investigate music. At the core of mingus is music theory, which includes topics like intervals, chords, scales and progressions. These components are rigurously tested and can be used to generate _and recognize_ musical elements using convenient shorthand where possible (for example some acceptable chords are: "CM7", "Am6", "Ab7", "G7").

### Bars, Tracks and Compositions ###

On top of the core are data structures (`mingus.containers`) that make it easier to work with notes in bars, tracks and compositions. These containers lay the foundation for the remaining packages: `midi` and `extra`.

### MIDI and Sequencing ###

The MIDI package can save and load MIDI files, and -last but not least- provides a general purpose sequencer for all the containers and a [FluidSynth](http://fluidsynth.resonance.org/trac) sequencer subclass. This allows you to play all your data structures straight from Python in just a couple of lines. Most of the icky timing and MIDI code has been abstracted away for you, leaving a clean, relatively simple API.

### Extra ###

Lastly, the extra package includes a [LilyPond](http://lilypond.org/web/) exporter which can be used to create sheet music in PDF, PNG and postscript. It also offers ASCII tablature and MusicXML exporting and a sound analysis module which can recognize notes and melody in raw audio data.


[Learn More About Mingus in the Wiki](mingusIndex.md)


---


## Latest news ##

  * _2011/28/03_ -- A Python3 version of mingus has become available at: http://code.google.com/r/artdent-mingus-python3/ . This work will soon be tied together  into a new mingus release with a couple of outstanding fixes and patches...so stay tuned :)

  * _2009/12/08_ -- Arun Chaganty converted the repository to mercurial, which will hopefully improve our development process. You can still see the old subversion repository [here](http://mingus.googlecode.com/svn/), but it will not be updated.

  * _2009/07/07_ -- Version 0.4.2.3: Features a new MusicXML module by Javier Palanca and a new SequencerObserver module that can be attached to a Sequencer. Also includes a full copy of the license, a THANKS and an AUTHORS file and updates to the copyright information; so that we can get included in the next Ubuntu release. [Release notes](http://groups.google.com/group/mingus-python/browse_thread/thread/f92b8fcb9e55f963).

  * _2009/07/02_ -- Version 0.4.2.0: Contains the new `tunings` module, with information about the different kind of tunings for various instruments, and the `tablature` module built on top of that, which can export all the mingus.containers to pretty ASCII tabs. See the [release notes](http://groups.google.com/group/mingus-python/browse_thread/thread/b5b5aca74e4f32f0) for more details and some examples.

[See the complete change log here](http://code.google.com/p/mingus/source/browse/trunk/CHANGELOG)


---


## Contact ##

For questions, patches, recommendations and requests, you can contact the [mingus google group](http://groups.google.com/group/mingus-python).

![http://groups.google.com/intl/en/images/logos/groups_logo_sm.gif](http://groups.google.com/intl/en/images/logos/groups_logo_sm.gif)

[Visit this group](http://groups.google.com/group/mingus-python)

### IRC ###

You can talk to us on freenode.net in the #mingus channel.