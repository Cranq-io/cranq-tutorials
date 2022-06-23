# Tag trimmer

[flow]

Trims the last iterable (colon-separated) section of the tag on the signal received via `data`.

Bounces when tag is not iterable.

Opposite of `flow/Tag nester`.

Used for lining up signals with iterations. (See eg. `data/array/Iterator`.)

Example:
1. "A"@"x:9" received via `data`
2. "A"@"x" is sent via `data` (output)

### Input ports:

* __data__: `any`
    Receives signal with iterable tag.



### Output ports:

* __data__: `any`
    Sends signal with data identical to the one received via `data`, but with the last iterable section removed from the tag.



* __bounced__: `any`
    Forwards the signal received through `data` when its tag was not iterable.



