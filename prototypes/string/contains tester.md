# Contains tester

[string]

Tests whether the value received via `string` contains the value received via `substring`.

Example:

1. "Quick brown fox"@0 is received via `string`
2. "brown"@0 is received via `substring`
3. true@0 is sent via `contains`

### Input ports:

* __string__: `string`
    The string to look for the substring in



* __substring__: `string`
    The string to find



### Output ports:

* __contains__: `boolean`
    Whether the string contains the substring



