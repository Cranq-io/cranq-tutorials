---
description: [flow]
---

# Repeater

Repeats the input the specified amount of times.

The tag on the repeat signals will contain the index of the current iteration.

Note that the repeats will be sent synchronously.

Example:
1. "A"@0 received via `data`
2. 3@0 received via `count`
3. "A"@"0:0" sent via `data`
4. "A"@"0:1" sent via `data`
5. "A"@"0:2" sent via `data`

### Input ports:

* __data__: `any`

    Receives data to be repeated.


* __count__: `number`

    Receives the number of times the input is to be repeated.

### Output ports:

* __data__: `any`

    Sends the repeated signal.

