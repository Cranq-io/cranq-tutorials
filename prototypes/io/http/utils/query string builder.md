# Query string builder

[io/http/utils]

Builds a query string by serializing the received dictionary as query params.

Example:
1. {"name": "Jane", "height": "1.63"}@1 received via `params`
2. "name=Jane&height=1.63"@1 sent via `query`

### Input ports:

* __params__: _{string: (string or string[])}_

    Receives query parameters to be serialized as a dictionary.



### Output ports:

* __query__: _string_

    Sends HTTP query string.


