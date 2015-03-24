
---


# mingus.extra.StringTuning #

StringTuning can be used to store and work with tunings and fingerings.


---


## Functions ##

### `__init__(self, instrument, description, tuning)` ###

  * `instrument` and `description` should be strings. tuning should be a list of strings or a list of lists of strings that denote courses. See tunings.add\_tuning for examples.

### `count_courses(self)` ###

  * Returns the average number of courses per string,

### `count_strings(self)` ###

  * Returns the number of strings.

### `find_chord_fingering(self, notes, max_distance, maxfret, return_best_as_NoteContainer)` ###

  * **Default values**: max\_distance = 4, maxfret = 18, return\_best\_as\_NoteContainer = False
  * Returns a list of fret lists that are considered possible fingerings. This function only looks at and matches on the note _names_ so it does more than `find_fingering`. For example: {{{
>>> t = tunings.get\_tuning("guitar", "standard", 6, 1)
>>> t.find\_chord\_fingering(NoteContainer().from\_chord("Am"))
[[0, 0, 2, 2, 1, 0],
> [0, 3, 2, 2, 1, 0], ......]
>>> t = tunings.StringTuning("test", "test", ["A-3", "E-4", "A-5"])
>>> t.find\_fingering(['E-4', 'B-4'])
[[(0, 7), (1, 7)], [(1, 0), (0, 14)]]
>>> t = tunings.StringTuning("test", "test", ["A-3", "E-4"])
>>> t.find\_frets(Note("C-4")
[3, None]
>>> t.find\_frets(Note("A-4")
[12, 5]
>>> t = tunings.StringTuning("test", "test", ['A-3', 'A-4'])
>>> t.find\_note\_names(["A", "C", "E"], 0, 12)
[(0, 'E'), (5, 'A'), (8, 'C'), (12, 'E')]
>>> t = tunings.StringTuning("test", "test", ['A-3', 'A-4'])
>>> t,get\_Note(0, 0)
'A-3'
>>> t.get\_Note(0, 1)
'A#-3'
>>> t.get\_Note(1, 0)
'A-4'}}}

=== `find_fingering(self, notes, max_distance, not_strings)` ===

  * *Default values*: max_distance = 4, not_strings = []
  * Returns a list [(string, fret)] of possible fingerings for `notes`. `notes` should be a list of strings or Notes or a !NoteContainer. `max_distance` denotes the maximum distance between frets. `not_strings` can be used to disclude certain strings and is used internally to recurse.
{{{
}}}

=== `find_frets(self, note, maxfret)` ===

  * *Default values*: maxfret = 24
  * Returns a list with for each string the fret on which the note is played or None if it can't be played on that particular string. `maxfret` is the highest fret that can be played. `note` should either be a string or a Note object. 
{{{
}}}

=== `find_note_names(self, notelist, string, maxfret)` ===

  * *Default values*: string = 0, maxfret = 24
  * Returns a list [(fret, notename)] in ascending order.
Notelist should be a list of Notes, note-strings or a NoteContainer.
{{{
}}}

=== `frets_to_NoteContainer(self, fingering)` ===

  * Converts a list such as returned by find_fret to a NoteContainer.

=== `get_Note(self, string, fret, maxfret)` ===

  * *Default values*: string = 0, fret = 0, maxfret = 24
  * Returns the Note on `string`, `fret`. Throws a RangeError if either the fret or string is unplayable.
{{{
}}}

----

[mingusIndex Back to Index]```