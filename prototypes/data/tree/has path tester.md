# Has path tester

[data/tree]

Tests whether a path is found in the specified tree data structure.

Example:
1. ["foo", "bar", "baz"]@0 is received via `path`
2. {"foo": { "bar": { "baz": 0 }}}@0 is received via `tree`
3. true@0 is sent via `has`

### Input ports:

* __path__: _(string or number)[]_

    The path to look for in the `tree`
    
    Example:
    
    ["foo", 1, "bar"] would match for the following `tree`:
    {"foo":[0, {"bar": "baz"}]}



* __tree__: _(any[] or {string: any})_

    The tree data structure to find the `path` within



### Output ports:

* __has__: _boolean_

    Whether the `path` was found in the `tree`



