#summary The mingus.containers.Suite module


---


# Tutorial 7 - Suite #

The Suite class can be used to store compositions together and will probably not be used as much (if you want to write a symphony, knock yourself out though).

## Import the Suite Class ##

```

>>> from mingus.containers.Suite import Suite

```


---


## Creating Suites ##

A Suite class takes no arguments to create:

```

>>> s = Suite()

```

## Setting Attributes ##

The following functions will set some useful attributes. Note however that the authors and titles won't be reset on the actual compositions, only on the Suite:

```

>>> s = Suite()
>>> s.set_author('Author', 'author@email.com')
>>> s.set_title('Title', 'Subtitle')


```



---


## Adding Compositions ##

```

>>> c = Composition()
>>> s = Suite()
>>> s.add_composition(c)

```


## List Notation ##

```

>>> c = Composition()
>>> len(c)
0
>>> c.add_composition(Composition())
>>> c[0] = Composition()
```



---


# End of Tutorial 7 #

You can learn more about [mingus.containers.Suite](refMingusContainersSuite.md) in the reference section.

  * [Tutorial 1 - The Note Class](tutorialNoteModule.md)
  * [Tutorial 2 - NoteContainers](tutorialNoteContainerModule.md)
  * [Tutorial 3 - Bars](tutorialBarModule.md)
  * [Tutorial 4 - Instruments](tutorialInstrumentModule.md)
  * [Tutorial 5 - Tracks](tutorialTrackModule.md)
  * [Tutorial 6 - Compositions](tutorialCompositionModule.md)
  * Tutorial 7 - Suites
  * [Back to Index](mingusIndex.md)