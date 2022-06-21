# Query param serializer

[io/http/utils]

Serializes the single query received via `param` as a key-value pair.

Example:
1. {"key": "name", "value": "Sally"}@1 received via `params`
2. "name=Sally"@1 sent via string

### Input ports:

* __param__: _{"key" :string, "value" :string}_

    Receives a single query parameter as key-value pair.



### Output ports:

* __string__: _string_

    Sends the serialized single query param.



