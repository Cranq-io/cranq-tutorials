---
description: [string]
---

# Splitter

Splits the  value received on `string` by the value received on `separator`.

Example:

1. "foo.bar.baz"@0 is received via `string`
2. "."@0 is received via `separator`
3. ["foo", "bar", "baz"]@0 is sent via `substrings`

### Input ports:

* __separator__: ` string `

    The separator string


* __string__: ` string `

    The string to be splitted

### Output ports:

* __substrings__: ` string[] `

    Sends the array of the parts.

