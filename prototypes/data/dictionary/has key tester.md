# Has key tester

[data/dictionary]

Tests whether a dictionary has a specific key.

Example A:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
2. "first"@0 received via `key`
3. `has` sends true@0

Example B:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
2. "second"@0 received via `key`
3. `has` sends false@0

### Input ports:

* __dict__: `{string: any}`

    Receives the dictionary to test.
    
    Example:
    { "first": 1, "third": 3, "fifth": 5 }


* __key__: `string`

    Receives the key to look for in the dictionary.
    
    Example:
    "first"

### Output ports:

* __has__: `boolean`

    Sends a value indicating whether the dictionary has the expected key.
    
    Example:
    true
    

