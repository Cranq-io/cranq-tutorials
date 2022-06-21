# Path serializer

[data/tree]

Serializes tree path, producing a canonically formatted path string.
Canonical tree paths are dot-separated, with dots inside components escaped with a backslash.

### Input ports:

* __path__: _(string or number)[]_

    Receives tree path. (Array of strings and numbers.)
    
    Example: ["foo", 0, "bar"]



### Output ports:

* __serialized__: _string_

    Sends a serialized tree path in canonical format.
    
    Examples:
    * "foo.bar.baz"
    * "foo"
    * "foo.b\\.r"



