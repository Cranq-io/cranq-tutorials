# Splitter

[string]

Splits the  value received on `string` by the value received on `separator`.

Example:

1. "foo.bar.baz"@0 is received via `string`
2. "."@0 is received via `separator`
3. ["foo", "bar", "baz"]@0 is sent via `substrings`

### Input ports:

* __separator__: _string_

    The separator string



* __string__: _string_

    The string to be splitted



### Output ports:

* __substrings__: _string[]_

    Sends the array of the parts.



