---
description: [flow]
---

# Tag nester

Creates a new level of iteration on the received tag, by appending ":0" to it.

Opposite of `flow/Tag trimmer`.

Used for lining up signals with iterations. (See eg. `data/array/Iterator`.)

Example:
1. "A"@0 received via `data`
2. "A"@"0:0" is sent via `data` (output)

See also:
* `flow/Tag incrementer`
* `flow/Tag trimer`

### Input ports:

* __data__: `any`

    Receives the signal to be nested.

### Output ports:

* __data__: `any`

    Sends signal with data identical to the one received via `data`, but with nested tag.

