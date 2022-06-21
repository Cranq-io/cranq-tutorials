# Single param appender

[io/http/utils]

Appends a single query parameter received via `key` and `value` to the array of single query params received via `params` (input), and sends the result via `params` (output).

Example:
1. "Sally"@1 received via `value`
2. "name"@1 received via `key`
3. []@1 received via `params`
4. [{"key": "name", "value": "Sally"}]@1 sent via `params` (output)

### Input ports:

* __value__: _string_

    Receives a single query parameter value.



* __key__: _string_

    Receives the key part of a key-value pair.



* __params__: _{"key" :string, "value" :string}[]_

    Receives an array of single query params as key-value pairs.



### Output ports:

* __params__: _{"key" :string, "value" :string}[]_

    Sends an array of single query params as key-value pairs.



