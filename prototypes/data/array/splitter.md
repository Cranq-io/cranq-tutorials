# Splitter

[data/array]

Create 2D array from 1D array.

Example:
1. [1,2,3]@0 recieved via  array`
2. 2@0 recieved via  `count`
3.  [[1,2],[3]]@0 sent via `array` 

### Input ports:

* __array__: _any_

    Receives array to be splitted.
    
    Example:
    [1,2,3,2]



* __count__: _any_

    Receives the size of the columns of the 2D array.
    
    Example:
    2



### Output ports:

* __2D array__: _any_

    Sends the created 2D array.
    
    Example:
    [[1,2],[3,4]]



