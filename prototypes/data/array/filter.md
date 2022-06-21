# Filter

[data/array]

Filters array. External node(s) receive each item and decide whether to include them in the result.

Example:
https://github.com/Cranq-io/cranq-tutorials/blob/main/reference/3_querying_data/3_2_filters/README.md#using-filters

### Input ports:

* __array__: _any[]_

    Receives array to be filtered.
    
    Example:
    [1,2,3,4]



* __include item__: _boolean_

    Receives whether to include the current (by tag) item.
    
    Example:
    true



### Output ports:

* __filtered__: _any[]_

    Sends the filtered array.
    
    Example:
    [1,2]



* __item__: _any[][number]_

    Sends the current item.
    
    Example:
    1



