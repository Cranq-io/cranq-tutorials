# URL search params serializer

[io/http]

Serializes URL search parameters.

Example:
1. { "term1": "foo", "term2": "bar"}@0 received on `params`
2. "term1=foo&term2=bar"@0 sent on `serialized`

1.[["term1", "foo"], ["term2", "bar"]]@0 received on `params`
2. "term1=foo&term2=bar"@0 sent on `serialized`

### Input ports:

* __params__: _({string: any} or [string,any][])_

    Received URL search parameters.
    
    Example:
    1. { "term1": "foo", "term2": "bar"}
    2. [["term1", "foo"], ["term2", "bar"]]



### Output ports:

* __serialized__: _string_

    Serialized parameters
    
    Example:
    "term1=foo&term2=bar"



