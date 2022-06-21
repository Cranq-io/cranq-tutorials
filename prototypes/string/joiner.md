# Joiner

[string]

Joins an ordered list of strings into a single string.

Example:

1. ["Hello", "!"]@0 is received via `substrings`
2. " world"@0 is received via `separator`
3. "Hello world!"@0 is sent via `joined`

### Input ports:

* __separator__: _string_

    The separator string



* __substrings__: _string[]_

    Array containing the parts



### Output ports:

* __joined__: _string_

    Sends the joined parts, separated by the separator string.



