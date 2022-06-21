# Mapper

[data/array]

Maps array. External node(s) receive each item and send back a mapped item.

Example:
https://github.com/Cranq-io/cranq-tutorials/blob/main/reference/3_querying_data/3_3_mappers/README.md#using-mappers

### Input ports:

* __array__: _any[]_

    Recieves array to be mapped.
    
    Example:
    ["Foo", "Bar"]



* __mapped item__: _any[][number]_

    Recieves the current (by tag) item, mapped.
    
    Example:
    "Foo A"



### Output ports:

* __mapped__: _any[][number][]_

    Sends the mapped array.
    
    Example:
    ["Foo A", "Bar A"]



* __item__: _any[][number]_

    Sends the current item.
    
    Example:
    "Foo"



* __index__: _number_



