# Reducer

[data/array]

Reduces array. External node(s) receive the partial result and each item and send back a new partial result.

Example:
https://github.com/Cranq-io/cranq-tutorials/blob/main/reference/3_querying_data/3_4_reducers/README.md#using-reducers

### Input ports:

* __array__: _any[]_

    Receives array to be reduced.
    
    Example:
    ["A", "B", "C"]



* __initial__: _any[][number]_

    Receives initial value for the reduced array
    
    Example:
    ""



* __part reduced__: _any[][number]_

    Receives reduced array before the current (by tag) item.
    
    Example:
    "AB"



### Output ports:

* __reduced__: _any[][number]_

    Sends the reduced array.
    
    Example:
    "ABC"



* __item__: _any[][number]_

    Sends the current item.
    
    Example:
    "C"



* __part reduced__: _any[][number]_

    Sends reduced array after the current (by tag) item.
    
    Example:
    "A"



