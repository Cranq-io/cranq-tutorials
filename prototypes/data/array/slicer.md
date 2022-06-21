# Slicer

[data/array]

Slices a section out of an array.

Example: 
1. [1,2,3]@0 received via `array`
2. 0@0 received via `from`
3. 2@0 received via `from`
4. [1,2]@0 sent via `array`

### Input ports:

* __array__: _any[]_

    Receives array to slice out of.
    
    Example:
    [1,2,3]



* __from__: _number_

    Receives start position of the slice (included).
    
    Example:
    0



* __to__: _number_

    Receives end position of the slice (not included.
    
    Example:
    2



### Output ports:

* __slice__: _any[]_

    Sends section sliced out of the input array.
    
    Example:
    [1,2]



