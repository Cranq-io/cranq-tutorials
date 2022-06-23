# Iterator

[data/tree]

Iterates over nodes in a tree (deeply nested object) structure, as specified by the query.
The `query` acts as a filter for the iteration. It could hold strings for object keys, numbers for array indices, or objects describing either catch-all or a set of keys to include.

An example `query`: ["foo", 1, {"type":"wildcard"}, {"type":"options", "options": ["bar", "baz"]}]

Example:
1. {"foo": [0, {"a": { "bar": 1 }, "b": { "baz": 1 }}]}@0 is received via `tree`
2.  ["foo", 1, {"type":"wildcard"}, {"type":"options", "options": ["bar", "baz"]}]@0 is received via `query`
3. ["foo", 1, "a", "bar"]@0:0 is sent via `path`
4. 1@0:0 is sent via `node`
5. the original `tree` is sent via `tree`
6. ["foo", 1, "a", "baz"]@0:1 is sent via `path`
7. 1@0:1 is sent via `node`
8. the original `tree` is sent via `tree`
9. null@0 is sent via `done`

### Input ports:

* __tree__: `(any[] or {string: any})`
    The tree data structure to iterate over on.



* __query__: 
    ```
    (string or number or {"type" :"wildcard"} or {"type" :"options", "options" :(string[] or number[])})[]
    ```

    Pattern for paths. Array of strings, numbers or expressions.
    Strings look for exact matches, numbers for array indices and expressions describe matching mechanisms.
    
    {"type": "wildcard"}
    Matches any key in the current node.
    
    {"type": "options", "options":[]}
    Matches the listed keys.



### Output ports:

* __path__: `(string or number)[]`
    Sends the current path in the iteration



* __node__: `any`
    Sends the current node in the iteration



* __tree__: `(any[] or {string: any})`
    Sends the entire tree



* __done__: `null`
    Sends null when the iteration is done



