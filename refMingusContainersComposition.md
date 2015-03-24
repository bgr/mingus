
---


# mingus.containers.Composition #

The Composition class is a datastructure for working with [Tracks](refMingusContainersTrack.md). Composition can be stored together in [Suites](refMingusContainersSuite.md).


---


## Attributes ##

### `author` ###

  * **Type**: str
  * **Value**: ''

### `email` ###

  * **Type**: str
  * **Value**: ''

### `selected_tracks` ###

  * **Type**: list
  * **Value**: [.md](.md)

### `subtitle` ###

  * **Type**: str
  * **Value**: ''

### `title` ###

  * **Type**: str
  * **Value**: 'Untitled'

### `tracks` ###

  * **Type**: list
  * **Value**: [.md](.md)


---


## Functions ##

### `__add__(self, value)` ###

  * Overloads the + operator for Compositions. Accepts [Notes](refMingusContainersNote.md), note strings, [NoteContainers](refMingusContainersNotecontainer.md), [Bars](refMingusContainersBar.md) and [Tracks](refMingusContainersTrack.md)

### `__getitem__(self, index)` ###

  * Overloads the [.md](.md) notation

### `__init__(self)` ###

### `__len__(self)` ###

  * Overloads the len() functions

### `__repr__(self)` ###

  * String representation of the class

### `__setitem__(self, index, value)` ###

  * Overloads the [.md](.md) = notation

### `add_note(self, note)` ###

  * Adds a note to the selected tracks. Accepts everything [container.Track](refMingusContainersTrack.md) supports in add

### `add_track(self, track)` ###

  * Adds a track to the composition. Raises an UnexpectedObjectError if the argument is not a [mingus.containers.Track](refMingusContainersTrack.md) object.

### `empty(self)` ###

  * Removes all the tracks from this class.

### `reset(self)` ###

  * Resets the information in this class. Removes the track and composer information.

### `set_author(self, author, email)` ###

  * **Default values**: author = '', email = ''
  * Sets the title and author of the piece

### `set_title(self, title, subtitle)` ###

  * **Default values**: title = 'Untitled', subtitle = ''
  * Sets the title and subtitle of the piece


---


[Back to Index](mingusIndex.md)