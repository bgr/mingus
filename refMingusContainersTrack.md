
---


# mingus.containers.Track #

The Track class can be used to store [Bars](refMingusContainersBar.md) and to work on them. The class is also designed to be used with [Instruments](refMingusContainersInstrument.md), but this is optional. Tracks can be stored together in [Compositions](refMingusContainersComposition.md)


---


## Attributes ##

### `bars` ###

  * **Type**: list
  * **Value**: [.md](.md)

### `instrument` ###

  * **Type**: NoneType
  * **Value**: None

### `name` ###

  * **Type**: str
  * **Value**: 'Untitled'

### `tuning` ###

  * **Type**: NoneType
  * **Value**: None


---


## Functions ##

### `__add__(self, value)` ###

  * Overloads the + operator for Tracks. Accepts [Notes](refMingusContainersNote.md), notes as string, [NoteContainers](refMingusContainersNotecontainer.md) and [Bars](refMingusContainersBar.md).

### `__eq__(self, other)` ###

  * Overloads the == operator for tracks.

### `__getitem__(self, index)` ###

  * Overloads the [.md](.md) notation for Tracks

### `__init__(self, instrument)` ###

  * **Default values**: instrument = None
### `__len__(self)` ###

  * Overloads the len() function for Tracks.

### `__repr__(self)` ###

  * The string representation of the class

### `__setitem__(self, index, value)` ###

  * Overloads the [.md](.md) = notation for Tracks. Throws an UnexpectedObjectError if the value being set is not a [mingus.containers.Bar](refMingusContainersBar.md) object.

### `add_bar(self, bar)` ###

  * Adds a [Bar](refMingusContainersBar.md) to the current track

### `add_notes(self, note, duration)` ###

  * **Default values**: duration = None
  * Adds a [Note](refMingusContainersNote.md), note as string or [NoteContainer](refMingusContainersNotecontainer.md) to the last [Bar](refMingusContainersBar.md). If the [Bar](refMingusContainersBar.md) is full, a new one will automatically be created. If the [Bar](refMingusContainersBar.md) is not full but the note can't fit in, this method will return `False`. True otherwise.

An InstrumentRangeError exception will be raised if an [Instrument](refMingusContainersInstrument.md) is attached to the Track, but the note turns out not to be within the range of the [Instrument](refMingusContainersInstrument.md).

### `augment(self)` ###

  * Calls augment on all the bars in the Track.

### `diminish(self)` ###

  * Calls diminish on all the bars in the Track.

### `from_chords(self, chords, duration)` ###

  * **Default values**: duration = 1
  * Adds chords to the Track. `chords` should be a list of shorthand strings or
list of list of shorthand strings, etc. Each sublist divides the value by 2. If a tuning is set,
chords will be expanded so they have a proper fingering.
```
>>> t = Track().from_chords(["C", ["Am", "Dm"], "G7", "C#"], 1)
```

### `get_tuning(self)` ###

  * Returns a StringTuning object. If an instrument is set and has a tuning it will be returned. Otherwise the track's one will be used.

### `set_tuning(self, tuning)` ###

  * Sets the tuning attribute on both the Track and its instrument (when available). Tuning should be a StringTuning or derivative object.

### `test_integrity(self)` ###

  * Test whether all but the last [Bars](refMingusContainersBar.md) contained in this track are full.

### `to_major(self)` ###

  * Calls to\_major on all the bars in the Track.

### `to_minor(self)` ###

  * Calls to\_minor on all the bars in the Track.

### `transpose(self, interval, up)` ###

  * **Default values**: up = True
  * Transposes all the notes in the track up or down the interval. Calls transpose() on every [Bar](refMingusContainersBar.md).


---


[Back to Index](mingusIndex.md)