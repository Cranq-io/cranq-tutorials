# Contains tester

[data/array]

Tests whether the array contains a given item

Example:
Example:
1. [1,2]@0 received via `array` 
2. 1@0 received via `item` 
3. true@0 sent via `contains`

### Input ports:

* __array__: _any[]_

    Recieves array look for the item in.
    
    Example:
    [1,2]



* __item__: _any_

    Recieves item to find in the array.
    
    Example:
     1



### Output ports:

* __contains__: _boolean_

    Sends whether the `item` was found in the `array`.
    
    Example:
    true



