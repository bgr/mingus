
---


# mingus.containers.Instrument #

The Instrument class is pretty self explanatory. Instruments can be used with [Tracks](refMingusContainersTrack.md) to define which instrument plays what, with the added bonus of checking whether the entered notes are in the range of the instrument.

It's probably easiest to subclass your own Instruments (see [Piano](refMingusContainersPiano.md) and [Guitar](refMingusContainersGuitar.md) for examples).


---


## Attributes ##

### `clef` ###

  * **Type**: str
  * **Value**: 'bass and treble'

### `name` ###

  * **Type**: str
  * **Value**: 'Instrument'

### `range` ###

  * **Type**: tuple
  * **Value**: ('C-0', 'C-8')

### `tuning` ###

  * **Type**: NoneType
  * **Value**: None


---


## Functions ##

### `__init__(self)` ###

### `__repr__(self)` ###

  * A string representation of the object

### `can_play_notes(self, notes)` ###

  * Will test if the notes lie within the range of the instrument. Returns `True` if so, `False` otherwise.

### `note_in_range(self, note)` ###

  * Tests whether note is in the range of this Instrument. Returns `True` if so, `False` otherwise

### `notes_in_range(self, notes)` ###

  * An alias for can\_play\_notes

### `set_range(self, range)` ###

  * Sets the range of the instrument. A range is a tuple of two [Notes](refMingusContainersNote.md) or note strings.


---


[Back to Index](mingusIndex.md)