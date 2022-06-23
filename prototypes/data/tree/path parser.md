# Path parser

[data/tree]

Parses a canonical string representation of a tree path. Tree paths are dot-separated, and dots in components are escaped with backslash.

Examples:
1. "foo.bar\.baz" is received via `path`
2. ["foo", "bar.baz"] is sent via `parsed`

### Input ports:

* __path__: `string`

    Receives a serialized tree path in canonical format.
    
    Examples:
    * "foo.bar.baz"
    * "foo"
    * "foo.b\\.r"

### Output ports:

* __parsed__: `(string or number)[]`

    Sends tree path. (Array of strings and numbers.)
    
    Example: ["foo", 0, "bar"]

