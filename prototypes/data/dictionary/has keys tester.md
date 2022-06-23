# Has keys tester

[data/dictionary]

Tests whether the key set of the dictionary contains the expected keys.

If `strict` is set, extra properties are not tolerated, the dictionary provided must have exactly the expected keys.

Example A:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
2. ["first", "fifth"]@0 received via `expected keys`
3. `strict` is set to false
4. `has` sends true@0

Example B:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
2. ["second", "seventh"]@0 received via `expected keys`
3. `strict` is set to false
4. `has` sends false@0

Example C:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
2. ["first", "fifth"]@0 received via `expected keys`
3. `strict` is set to true
4. `has` sends false@0

### Input ports:

* __dict__: `{string: any}`
    Receives the dictionary to test.
    
    Example:
    { "first": 1, "third": 3, "fifth": 5 }



* __expected keys__: `string[]`
    Receives an array of expected keys.
    
    Example:
    [ "first", "third" ]



* __strict__: `boolean`
    Receives whether extra keys in `dict` are allowed.
    
    Example:
    false



### Output ports:

* __has__: `boolean`
    Sends a value indicating whether the dictionary has the expected keys.
    
    Example:
    true
    



