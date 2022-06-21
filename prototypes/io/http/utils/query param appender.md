# Query param appender

[io/http/utils]

Appends a single or array query param received via `param` to the received list of single query `params` in a key-value pair format.

Example:
1. {"key": "name", "value": ["John", "Doe"]}@1 received via `param`
2. [{"key": "age", "value": "27"}]@1 received via `params`
3. [{"key": "age", "value": "27"}, {"key": "name", "value": "John"}, {"key": "name", "value": "Doe"}]@1 sent via `params` (output)

### Input ports:

* __param__: _{"key" :string, "value" :(string or string[])}_

    Receives a query parameter as a key-value pair. The query parameter may be a single value or an array.



* __params__: _{"key" :string, "value" :string}[]_

    Receives an array of single parameter key-value pairs.



### Output ports:

* __params__: _{"key" :string, "value" :string}[]_

    Sends an array of single query parameters as key-value pairs.



