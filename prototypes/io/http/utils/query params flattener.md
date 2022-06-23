---
description: io/http/utils]
---

# Query params flattener

Flattens query parameters received via `params` expressed as a dictionary, into an array of single query parameters as key-value pairs sent via `flattened`.

Example:
1. [{"key": "name", "value": "Sophie"}, {"key": "friends", "value": ["Liya", "Owen"]}]@1 received via `params`
2. [{"key": "name", "value": "Sophie"}, {"key": "friends", "value": "Liya"}, {"key": "friends", "value": "Owen"}]@1 sent via `flattened`


### Input ports:

* __params__: `{string: (string or string[])}`

    Receives query parameters as dictionary.

### Output ports:

* __flattened__: `{"key" :string, "value" :string}[]`

    Sends query parameter key-value pairs individually.

