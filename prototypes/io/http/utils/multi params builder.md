# Multi params builder

[io/http/utils]

Builds an array of single query parameters as key-value pairs based on the key received via `key` and the values received via `values`.

Example:
1. ["Norah", "Smith"]@1 received via `values`
2. "name"@1 received via `key`
3. [{"key": "name", "value": "Norah"}, {"key": "name", "value": "Smith"}]@1 sent via `params`

### Input ports:

* __values__: `string[]`
    Receives an array of query parameter values associated with the same key.



* __key__: `string`
    Receives the key part of a key-value pair.



### Output ports:

* __params__: `{"key" :string, "value" :string}[]`
    Sends an array of single query params as key-value pairs.



