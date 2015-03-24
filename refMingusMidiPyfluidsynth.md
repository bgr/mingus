
---


# mingus.midi.pyFluidSynth #





---


## Attributes ##

### `DEFAULT_MODE` ###

  * **Type**: int
  * **Value**: 0

### `RTLD_GLOBAL` ###

  * **Type**: int
  * **Value**: 256

### `RTLD_LOCAL` ###

  * **Type**: int
  * **Value**: 0

### `api_version` ###

  * **Type**: str
  * **Value**: '1.2'

### `cdll` ###

  * **Type**: ctypes.LibraryLoader
  * **Value**: <ctypes.LibraryLoader object at 0x2726490>

### `lib` ###

  * **Type**: str
  * **Value**: 'libfluidsynth.so.1'

### `pydll` ###

  * **Type**: ctypes.LibraryLoader
  * **Value**: <ctypes.LibraryLoader object at 0x27264d0>

### `pythonapi` ###

  * **Type**: ctypes.PyDLL
  * **Value**: <PyDLL 'None', handle 7fce244c4000 at 2726510>


---


## Functions ##

### `ARRAY(typ, len)` ###

### `CFUNCTYPE(restype)` ###

  * CFUNCTYPE(restype, **argtypes,
> > use\_errno=False, use\_last\_error=False) -> function prototype.**


> restype: the result type
> argtypes: a sequence specifying the argument types

> The function prototype can be called in different ways to create a
> callable object:

> prototype(integer address) -> foreign function
> prototype(callable) -> create and return a C callable function from callable
> prototype(integer index, method name[, paramflags]) -> foreign function calling a COM method
> prototype((ordinal number, dll object)[, paramflags]) -> foreign function exported by ordinal
> prototype((function name, dll object)[, paramflags]) -> foreign function exported by name


### `PYFUNCTYPE(restype)` ###

### `SetPointerType(pointer, cls)` ###

### `c_buffer(init, size)` ###

  * **Default values**: size = None
### `cast(obj, typ)` ###

### `cfunc(name, result)` ###

  * Build and apply a ctypes prototype complete with parameter flags

### `create_string_buffer(init, size)` ###

  * **Default values**: size = None
  * create\_string\_buffer(aString) -> character array
> > create\_string\_buffer(anInteger) -> character array
> > create\_string\_buffer(aString, anInteger) -> character array


### `create_unicode_buffer(init, size)` ###

  * **Default values**: size = None
  * create\_unicode\_buffer(aString) -> character array
> > create\_unicode\_buffer(anInteger) -> character array
> > create\_unicode\_buffer(aString, anInteger) -> character array


### `find_library(name)` ###

### `fluid_synth_write_s16_stereo(synth, len)` ###

  * Return generated samples in stereo 16-bit format


> Return value is a Numpy array of samples.



### `raw_audio_string(data)` ###

  * Return a string of bytes to send to soundcard

> Input is a numpy array of samples.  Default output format
> is 16-bit signed (other formats not currently supported).



### `string_at(ptr, size)` ###

  * **Default values**: size = -1
  * string\_at(addr[, size]) -> string

> Return the string at addr.

### `wstring_at(ptr, size)` ###

  * **Default values**: size = -1
  * wstring\_at(addr[, size]) -> string

> Return the string at addr.


---


[Back to Index](mingusIndex.md)