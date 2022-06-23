# URL search params serializer

[io/http]

Serializes URL search parameters.

Example:
1. { "term1": "foo", "term2": "bar"}@0 received on `params`
2. "term1=foo&term2=bar"@0 sent on `serialized`

1.[["term1", "foo"], ["term2", "bar"]]@0 received on `params`
2. "term1=foo&term2=bar"@0 sent on `serialized`

### Input ports:

* __params__: `({string: any} or [string,any][])`

    Received URL search parameters.
    
    Example:
    1. { "term1": "foo", "term2": "bar"}
    2. [["term1", "foo"], ["term2", "bar"]]

### Output ports:

* __serialized__: `string`

    Serialized parameters
    
    Example:
    "term1=foo&term2=bar"

