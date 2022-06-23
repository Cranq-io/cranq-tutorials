---
description: [number]
---

# Greater than tester

Checks if the value received on `value` is greater than the value received on `reference`. If the values are equal, it outputs false.

Example:

1. 20@0 is received via `value`
2. 19@0 is received via `reference`
3. true@0 is sent via `greater`

### Input ports:

* __value__: `number`

    The first operand of the comparison.


* __reference__: `number`

    The second operand of the comparison.

### Output ports:

* __is greater__: `boolean`

    Sends true if "a" is greater than "b"

