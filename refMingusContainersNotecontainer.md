
---


# mingus.containers.NoteContainer #

The NoteContainer provides a container for the [mingus.containers.Note](refMingusContainersNote.md) objects. It can be used to store single and multiple notes in and is required for working with [Bars](refMingusContainersBar.md).


---


## Attributes ##

### `notes` ###

  * **Type**: list
  * **Value**: [.md](.md)


---


## Functions ##

### `__add__(self, notes)` ###

  * This method allows you to use '+' notation on NoteContainers.
> Example:
```
>>> n = NoteContainer(["C", "E", "G"])
>>> n + "B"
["C-4", "E-4", "G-4", "B-4"] 
```

### `__eq__(self, other)` ###

  * Overloads the == operator for NoteContainer instances.

### `__getitem__(self, item)` ###

  * This method allows you to use the container as a simple array.
> Example:
```
>>> n = NoteContainer(["C", "E", "G"])
>>> n[0]
'C-4' 
```


### `__init__(self, notes)` ###

  * **Default values**: notes = [.md](.md)
### `__len__(self)` ###

  * Returns the number of notes in the container

### `__repr__(self)` ###

  * A nice and clean string representation of the note container

### `__setitem__(self, item, value)` ###

  * This allows you to use [.md](.md) notation on NoteContainers. This function accepts Notes and notes as string.
> Examples:
```
>>> n = NoteContainer(["C", "E", "G"])
>>> n[0] = "B"
["B-5", "E-5", "G-5"] 
```

### `__sub__(self, notes)` ###

  * This method allows you to use the '-' operator on NoteContainers.
> Example:
```
>>> n = NoteContainer(["C", "E", "G"])
>>> n - "E"
["C-4", "G-4"]
```

### `_consonance_test(self, testfunc, param)` ###

  * **Default values**: param = None
  * Private function used for testing consonance/dissonance.

### `add_note(self, note, octave, dynamics)` ###

  * **Default values**: octave = None, dynamics = {}
  * Adds a note to the container and sorts the notes from low to high. The note can either be a string, in which case you could also use the octave and dynamics arguments, or a Note object.

### `add_notes(self, notes)` ###

  * Feeds notes to self.add\_note. The notes can either be an other NoteContainer, a list of [Note](refMingusContainersNote.md) objects or strings or a list of lists formatted like this:
```
notes = [["C", 5], ["E", 5], ["G", 6]] 
```
> or even:
```
notes = [["C", 5, {"volume" : 20}], ["E", 6, {"volume":20}]]
```

### `augment(self)` ###

  * Augments all the notes in the NoteContainer

### `determine(self, shorthand)` ###

  * **Default values**: shorthand = False
  * Determines the type of chord or interval currently in the container

### `diminish(self)` ###

  * Diminishes all the notes in the NoteContainer

### `empty(self)` ###

  * Empties the container.

### `from_chord(self, shorthand)` ###

  * Shortcut to from\_chord\_shorthand.

### `from_chord_shorthand(self, shorthand)` ###

  * Empties the container and adds the notes in the shorthand. See mingus.core.chords.from\_shorthand for an up to date list of recognized format.
```
>>> nc = NoteContainer()
>>> nc.from_chord_shorthand("Am")
['A-4', 'C-5', 'E-5']
```

### `from_interval(self, startnote, shorthand, up)` ###

  * **Default values**: up = True
  * Shortcut to from\_interval\_shorthand.

### `from_interval_shorthand(self, startnote, shorthand, up)` ###

  * **Default values**: up = True
  * Empties the container and adds the note described in the startnote and shorthand. See core.intervals for the recognized format.
```
>>> nc = NoteContainer()
>>> nc.from_interval_shorthand("C", "5")
['C-4', 'G-4']
>>> nc.from_interval_shorthand(("C", "5", False)
['F-3', 'C-4']
```

### `from_progression(self, shorthand, key)` ###

  * **Default values**: key = 'C'
  * Shortcut to from\_progression\_shorthand.

### `from_progression_shorthand(self, shorthand, key)` ###

  * **Default values**: key = 'C'
  * Empties the container and adds the notes described in the progressions shorthand (eg. 'IIm6', 'V7', etc). See mingus.core.progressions for all the recognized format.
```
>>> nc = NoteContainer()
>>> nc.from_progression_shorthand("VI")
['A-4', 'C-5', 'E-5']
```

### `get_note_names(self)` ###

  * Returns a list with all the note names in the current container. Every name will only be mentioned once.

### `is_consonant(self, include_fourths)` ###

  * **Default values**: include\_fourths = True
  * Tests whether the notes are consonants. See the core.intervals module for a longer description on consonance.

### `is_dissonant(self, include_fourths)` ###

  * **Default values**: include\_fourths = False
  * Tests whether the notes are dissonants. See the core.intervals module for a longer description.

### `is_imperfect_consonant(self)` ###

  * Tests whether the notes are imperfect consonants. See the core.intervals module for a longer description on consonance.

### `is_perfect_consonant(self, include_fourths)` ###

  * **Default values**: include\_fourths = True
  * Tests whether the notes are perfect consonants. See the core.intervals module for a longer description on consonance.

### `remove_duplicate_notes(self)` ###

  * A helper function that removes duplicate and enharmonic notes from the container

### `remove_note(self, note, octave)` ###

  * **Default values**: octave = -1
  * Removes note from container. The note can either be a [Note](refMingusContainersNote.md) object or a string representing the note's name. If no specific octave is given, the note gets removed in every octave.

### `remove_notes(self, notes)` ###

  * Removes notes from the containers. This function accepts a list of [Note](refMingusContainersNote.md) objects or notes as strings and also single strings or [Note](refMingusContainersNote.md) objects.

### `sort(self)` ###

  * Sorts the notes in the container from low to high.

### `to_major(self)` ###

  * Converts all the notes in the container to their major equivalent.

### `to_minor(self)` ###

  * Converts all the notes in the container to their minor equivalent.

### `transpose(self, interval, up)` ###

  * **Default values**: up = True
  * Transposes all the notes in the container up or down the given interval.


---


[Back to Index](mingusIndex.md)