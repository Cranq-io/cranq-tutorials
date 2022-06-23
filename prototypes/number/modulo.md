---
description: number]
---

# Modulo

Takes modulo of 'a' and 'b'. Bounces synced operands on division by zero.

Example:

1. 10@0 is received via `a`
2. 9@0 is received via `b`
3. 1@0 is sent via `remainder`

### Input ports:

* __a__: `number`

    The divident of the operation.


* __b__: `number`

    The divisor of the operation.

### Output ports:

* __remainder__: `number`

    The remainder of the operation.


* __bounced__: `{"a" :number, "b" :number}`

    Sends synced inputs on error.

