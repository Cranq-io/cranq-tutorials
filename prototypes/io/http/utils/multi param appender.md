# Multi param appender

[io/http/utils]

Appends a query parameter with multiple values received via `key` and `values` to the array of single query params received via `params` (input), and sends the result via `params` (output).

Example:
1. "Sally"@1 received via `value`
2. "name"@1 received via `key`
3. []@1 received via `params`
4. [{"key": "name", "value": "Sally"}]@1 sent via `params` (output)

### Input ports:

* __values__: `string[]`

    Receives values associated with the same query parameter.


* __key__: `string`

    Receives the key part of a key-value pair.


* __params__: `{"key" :string, "value" :string}[]`

    Receives an array of single query params as key-value pairs.

### Output ports:

* __params__: `{"key" :string, "value" :string}[]`

    Sends an array of single query params as key-value pairs.

