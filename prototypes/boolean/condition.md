# Condition

[boolean]

Sends either on the `true` or the `false` output port, depending on the input value received on the `boolean` port.

Example:

1. true@0 is received on `boolean`
2. null@0 is sent via `true`

### Input ports:

* __boolean__: _boolean_

    Input condition value



### Output ports:

* __true__: _null_

    Sends null if the input value is true.



* __false__: _null_

    Sends null if the input value is false.



