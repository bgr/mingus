
---


# mingus.containers.Bar #

A Bar is basically a container for [NoteContainers](refMingusContainersNotecontainer.md) (a NoteContainerContainer if you will, but you shouldn't). Bars can be stored together with [Instruments](refMingusContainersInstrument.md) in [Tracks](refMingusContainersTrack.md).


---


## Attributes ##

### `bar` ###

  * **Type**: list
  * **Value**: [.md](.md)

### `current_beat` ###

  * **Type**: float
  * **Value**: 0.0

### `key` ###

  * **Type**: str
  * **Value**: 'C'

### `length` ###

  * **Type**: float
  * **Value**: 0.0

### `meter` ###

  * **Type**: tuple
  * **Value**: (4, 4)


---


## Functions ##

### `__add__(self, note_container)` ###

  * Enables the '+' operator on Bars

### `__eq__(self, other)` ###

  * Overloads the '==' operator for Bars

### `__getitem__(self, index)` ###

  * Allows you to use `Bar[]` notation on Bars to get the item at the index.

### `__init__(self, key, meter)` ###

  * **Default values**: key = 'C', meter = (4, 4)
### `__len__(self)` ###

  * Overloads the len() method for Bars

### `__repr__(self)` ###

  * Enables str() and repr() for Bars

### `__setitem__(self, index, value)` ###

  * Allows you to use [.md](.md) = notation on Bars. The value should be a [NoteContainer](refMingusContainersNotecontainer.md), or a string/list/[Note](refMingusContainersNote.md) understood by the [NoteContainer](refMingusContainersNotecontainer.md).

### `augment(self)` ###

  * Calls augment on the NoteContainers in Bar.

### `change_note_duration(self, at, to)` ###

  * Changes the note duration at index `at` to duration `to`

### `determine_chords(self, shorthand)` ###

  * **Default values**: shorthand = False
  * Returns a list of lists [place\_in\_beat, possible\_chords].

### `determine_progression(self, shorthand)` ###

  * **Default values**: shorthand = False
  * Returns a list of lists [place\_in\_beat, possible\_progressions].

### `diminish(self)` ###

  * Calls diminish on the NoteContainers in Bar.

### `empty(self)` ###

  * Empties the Bar, removes all the [NoteContainers](refMingusContainersNotecontainer.md)

### `get_note_names(self)` ###

  * Returns a list of unique note names in the Bar.

### `get_range(self)` ###

  * Returns the highest and the lowest note in a tuple

### `is_full(self)` ###

  * Returns False if there is room in this Bar for another [NoteContainer](refMingusContainersNotecontainer.md), True otherwise.

### `place_notes(self, notes, duration)` ###

  * Places the notes on the `current_beat`. Notes can be strings, [Notes](refMingusContainersNote.md), list of strings, list of [Notes](refMingusContainersNote.md) or a [NoteContainer](refMingusContainersNotecontainer.md). Raises a MeterFormatError if the duration is not valid. Returns True if succesful, False otherwise (ie. the Bar hasn't got enough room for a note of that duration.)

### `place_notes_at(self, notes, at)` ###

  * Places notes at the index `at`

### `place_rest(self, duration)` ###

  * Places a rest of `duration` on the `current_beat`. The same as `place_notes(None, duration)`

### `remove_last_entry(self)` ###

  * Removes the last [NoteContainer](refMingusContainersNotecontainer.md) in the Bar

### `set_meter(self, meter)` ###

  * Meters in mingus are represented by a single tuple. This function will set the meter of this bar. If the format of the meter is not recognised, a MeterFormatError will be raised.

### `space_left(self)` ###

  * Returns the space left on the Bar.

### `to_major(self)` ###

  * Calls to\_major on the NoteContainers in Bar.

### `to_minor(self)` ###

  * Calls to\_minor on the NoteContainers in Bar.

### `transpose(self, interval, up)` ###

  * **Default values**: up = True
  * Transposes the notes in the bar up or down the interval. Calls transpose() on all [NoteContainers](refMingusContainersNotecontainer.md) in the bar.

### `value_left(self)` ###

  * Returns the value left on the Bar.


---


[Back to Index](mingusIndex.md)