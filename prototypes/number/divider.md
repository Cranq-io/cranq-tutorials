# Divider

[number]

Divides the received inputs. Bounces synced operands on division by zero.

Example (valid division):

1. 1@0 is received via `a`
2. 2@0 is received via `b`
3. 0.5@0 is sent via `fraction`

Example (divide by zero):

1. 13@0 is received via `a`
2. 0@0 is received via `b`
3. {"a":13, "b":0}@0 is sent via `bounced`

### Input ports:

* __a__: `number`

    The counter part of the fraction.


* __b__: `number`

    Denominator part of the fraction.

### Output ports:

* __fraction__: `number`

    The fraction of the received numbers.


* __bounced__: `{"a" :number, "b" :number}`

    Sends synced inputs on error.

