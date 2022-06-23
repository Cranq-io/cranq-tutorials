---
description: [flow]
---

# Tag incrementer

Increments the iterable (colon-separated) part of the received signal's tag.

Bounces when tag is not iterable.

Used for lining up signals with iterations. (See eg. `data/array/Iterator`.)

Example A (success):
1. "A"@"x:1" received via `data`
2. "A"@"x:2" is sent via `data` (output)

Example B (invalid input):
1. "A"@"x" received via `data`
2. "A"@"x" is sent via `bounced`

See also:
* `flow/Tag nester`
* `flow/Tag trimer`

### Input ports:

* __data__: `any`

    Receives signal with iterable tag.
    
    When the tag is not iterable, the signal will be bounced.

### Output ports:

* __data__: `any`

    Sends signal with data identical to the one received via `data`, but with incremented tag.


* __bounced__: `any`

    Forwards the signal received through `data` when its tag was not iterable.

