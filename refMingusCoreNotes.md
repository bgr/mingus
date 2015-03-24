
---


# mingus.core.notes #



> This module is the foundation of the music theory package.
> It handles conversions from integers to notes and vice versa and thus
> enables simple calculations. You should note however, that the
> int\_to\_note conversion can't be correctly done without knowing
> exactly what key we are in and what augmentations are being used.
> The same function in other modules ([diatonics](refMingusCoreDiatonic.md)
> and [container.Note](refMingusContainersNote.md)) will
> do a better _theoretical_ job at int\_to\_note, but this one is
> still usable for simple representations and trackers, etc. where
> keys don't really matter.




---


## Attributes ##

### `fifths` ###

  * **Type**: list
  * **Value**: ['F', 'C', 'G', 'D', 'A', 'E', 'B']


---


## Functions ##

### `augment(note)` ###

  * Augments a given note.
> Examples:
```
>>> augment("C")
'C#'
>>> augment("Cb") 
'C'
```

### `diminish(note)` ###

  * Diminishes a given note.
> Examples:
```
>>> diminish("C") 
'Cb'
>>> diminish("C#") 
'C'
```

### `int_to_note(note_int)` ###

  * Converts integers in the range of 0-11 to notes in the form of C or C# (no Cb). You can use int\_to\_note in diatonic\_key to do theoretically correct conversions that bear the key in mind. Throws a RangeError exception if the note\_int is not in range(0,12).

### `is_enharmonic(note1, note2)` ###

  * Test whether note1 and note2 are enharmonic, ie. they sound the same

### `is_valid_note(note)` ###

  * Returns true if note is in a recognised format. False if not

### `note_to_int(note)` ###

  * Converts notes in the form of C, C#, Cb, C##, etc. to an integer in the range of 0-11. Throws an NoteFormatError exception if the note format is not recognised.

### `remove_redundant_accidentals(note)` ###

  * Removes redundant #'s and b's from the given note. For example: C##b becomes C#, Eb##b becomes E, etc.

### `to_major(note)` ###

  * Returns the major of `note`.
> Example:
```
>>> to_major("A") 
'C'
```

### `to_minor(note)` ###

  * Returns the minor of note.
> Example:
```
>>> to_minor("C")
'A'
```


---


[Back to Index](mingusIndex.md)