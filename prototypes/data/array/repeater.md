# Repeater

[data/array]

Repeats the input data for each item in the array.

Example:
1. [1,2,3]@0 receiced via `array`
2. "foo"@0 received via `data`
3. "foo"@0:0
    "foo"@0:1
    "foo"@0:2
sent via `data`
    

### Input ports:

* __array__: _any[]_

    Recieves array which specifies number of times to repeat data.
    
    Example:
    [1,2,3]



* __data__: _any_

    Recieves data to be repeated.
    
    Example:
    "foo"



### Output ports:

* __data__: _any_

    Sends repeated data with tag.
    
    Example:
    "foo"


