# Global regex matcher

[string]

Executes a global regex pattern match.

Flavour depends on the running environment.

### Input ports:

* __string__: `string`

    The string.


* __regex__: `string`

    The regex pattern

### Output ports:

* __matches__: `boolean`

    Whether the given regex matches the given string


* __groups__: `string[]`

    Groups matched by the given regex pattern

