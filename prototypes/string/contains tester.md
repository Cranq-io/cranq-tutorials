# Contains tester

[string]

Tests whether the value received via `string` contains the value received via `substring`.

Example:

1. "Quick brown fox"@0 is received via `string`
2. "brown"@0 is received via `substring`
3. true@0 is sent via `contains`

### Input ports:

* __string__: _string_

    The string to look for the substring in



* __substring__: _string_

    The string to find



### Output ports:

* __contains__: _boolean_

    Whether the string contains the substring



