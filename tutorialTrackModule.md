#summary The mingus.containers.Track module


---


# Tutorial 5 - Tracks #

The Track class is a simple data structure to store [Bars](tutorialBarModule.md) in. The Class can also be used with an [Instrument](tutorialInstrumentModule.md), but this is optional.

## Import the Track Class ##

```

>>> from mingus.containers.Track import Track

```


---


## Creating Tracks ##

To create a new track you can simply make a new instance of `Track()`. If you want to have Instrument support, with automatic range checking, etc. you should give that as an argument:

```

>>> t = Track()
>>> t = Track(Instrument())

```



---


## Adding Bars ##

Adding bars can be done using `add_bar`.

```

>>> b = Bar()
>>> t = Track()
>>> t.add_bar(b)

```

## Adding Notes and NoteContainers ##

Adding notes to a track can be done using `add_notes`. This function accepts Notes, notes as strings and NoteContainers and adds them to the last Bar. If the [Bar](refMingusContainersBar.md) is full, a new one will automatically be created. If the [Bar](refMingusContainersBar.md) is not full but the note can't fit in, this method will return `False`. True otherwise.

Also, when an Instrument is attached to the Track, but the note turns out not to be within the range of that Instrument, an InstrumentRangeError will be raised.

```

>>> t = Track()
>>> t.add_notes("C")
True

```

## The overloaded '+' operator ##

This should be familiar stuff by now, but the '+' operator is overloaded for the Track class as well and accepts strings, NoteContainers, Notes and Bars.

```

>>> t = Track()
>>> b = Bar()
>>> t + b
>>> t + "C-4"
True

```


---


## List Notation ##

Tracks, like Bars and NoteContainers can be used as lists as well.

```
>>> t = Track()
>>> b = Bar()
>>> b + "C"
True
>>> t + b
True
>>> t[0]
[[0.0, 4, ["C-4"]]]
>>> t[0] = Bar()
>>> t[0]
[[]]

```


---


## Other Methods ##

The usual methods: -transpose, augment, diminish, to\_major and to\_minor- are also available on Tracks. Calls to these functions will get redirected to each Bar's equivalent.


---


# End of Tutorial 5 #

You can learn more about [mingus.containers.Track in the reference section](refMingusContainersTrack.md)

  * [Tutorial 1 - The Note Class](tutorialNoteModule.md)
  * [Tutorial 2 - NoteContainers](tutorialNoteContainerModule.md)
  * [Tutorial 3 - Bars](tutorialBarModule.md)
  * [Tutorial 4 - Instruments](tutorialInstrumentModule.md)
  * Tutorial 5 - Tracks
  * [Tutorial 6 - Compositions](tutorialCompositionModule.md)
  * [Back to Index](mingusIndex.md)