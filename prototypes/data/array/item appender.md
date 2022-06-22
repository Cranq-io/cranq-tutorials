# Item appender

[data/array]

Appends item to the array.

Example: 
1. [1,2,3]@0 recieved via `array` 
2. 1@0 recieved via `item` 
3. [1,2,3,1]@0 sent via `array`

### Input ports:

* __array__: _any[]_

    Receives array to append item to.
    
    Example:
    [1,2,3]



* __item__: _any_

    Receives item to append to the array.
    
    Example:
    1



### Output ports:

* __array__: _any[]_

    Sends the new array with the appended item.
    
    Example:
    [1,2,3,1]


