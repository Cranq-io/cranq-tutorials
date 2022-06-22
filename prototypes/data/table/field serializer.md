# Field serializer

[data/table]

Serializes field values in the table received via `table`.

Example:
1. [{"foo": 1, "bar": [1, 2]}]@1 received via `table`
2. [{"foo": 1, "bar": "[1,2]"}]@1 sent via `table` (output)

### Input ports:

* __table__: _{string: any}[]_

    [Inherited from port `array` of `mapper`] 
    Recieves array to be mapped.
    
    Example:
    ["Foo", "Bar"]



### Output ports:

* __table__: _{string: (string or number or boolean or null)}[]_


