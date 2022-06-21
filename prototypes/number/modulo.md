# Modulo

[number]

Takes modulo of 'a' and 'b'. Bounces synced operands on division by zero.

Example:

1. 10@0 is received via `a`
2. 9@0 is received via `b`
3. 1@0 is sent via `remainder`

### Input ports:

* __a__: _number_

    The divident of the operation.



* __b__: _number_

    The divisor of the operation.



### Output ports:

* __remainder__: _number_

    The remainder of the operation.



* __bounced__: _{"a" :number, "b" :number}_

    Sends synced inputs on error.



