# Flattener

[data/tree]

Flattens a tree into a flat dictionary with keys created by prepending parent keys and a delimiter to child keys recursively.

Example:

1. {"a": {"a1": 1, "a2":2}}@0 is received via `tree`
2. "-"@0 is received via `delimiter`
3. {"a-a1": 1, "a-a2":2}@0 is sent via `flattened`

### Input ports:

* __tree__: `(any[] or {string: any})`
    The tree to flatten



* __delimiter__: `string`
    The delimiter to use when prepending parent keys to child keys



### Output ports:

* __flattened__: `{string: any}`
    The flat dictionary



