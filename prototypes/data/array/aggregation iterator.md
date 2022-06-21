# Aggregation iterator

[data/array]

Iterates through items of an array, specifically for the purpose of being aggregated later.

### Input ports:

* __array__: _any[]_

    Recieves array to be iterated over.
    
    Example:
    [1,2,3]



### Output ports:

* __item__: _any[][number]_

    Sends current item.
    
    Example:
    1



* __is last__: _boolean_

    Sends flag whether current item is the last one.
    
    To be connected directly to the `release` input of a `flow/Aggregator`.



