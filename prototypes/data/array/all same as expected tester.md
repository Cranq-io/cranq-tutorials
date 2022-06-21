# All same as expected tester

[data/array]

Tests whether all elements of an array are the same as the expected value.

Example:
1. `array` recieved  [1,1]@0  
2. `expected` recieved  1]@0  
3.  true@0 sent via `same`

### Input ports:

* __array__: _any_

    Receives array to be tested.
    
    Example: 
    [1,2,3]



* __expected__: _any_

    Receives the expected value that all elements of the array will be tested against.
    
    Example:
    1



### Output ports:

* __same__: _boolean_

    Sends whether all elements of the `array` are the same as the `expected` value.
    
    Example:
    true



