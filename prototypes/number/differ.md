# Differ

[number]

Sends the difference of the last two numbers received. The (n-1)th number will be subtracted from the nth number.

Example:
1. 10@0 is received via `number`
2. 20@1 is received via `number`
3. 10@1 is sent via `diff`

### Input ports:

* __number__: _number_

    Receives numbers to be subtracted



### Output ports:

* __diff__: _number_

    The difference of the last two numbers received.



