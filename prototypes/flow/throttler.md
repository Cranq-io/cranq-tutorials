---
description: [flow]
---

# Throttler

Throttles the received signal, forwarding only `count` number of signals in `delay` milliseconds.

Reports internal buffer size via `buffer size`.

Example:
1. `delay` set to 3000, `count` set to 1 
1. A@1 received via `data`
2. B@2 received via `data` a second later
3. B@2 sent immediately via `data`
4. C@3 received via `data`
5. 1@3 sent via `buffer size`
6. C@3 sent via `data` a second later
6. 0@3 sent via `buffer size`


### Input ports:

* __data__: `any`

    Receives data to be throttled / rate limited.


* __delay__: `number`

    Receives the length of the time window in milliseconds, in which to limit the number of signals.
    
    Can be set as parameter.


* __count__: `number`

    Receives the maximum number of signals to be forwarded in the specified time window.
    
    Can be set as parameter.

### Output ports:

* __data__: `any`

    Forwards the signals received via `data`, throttled.


* __buffer size__: `number`

    Sends the current size of the throttler's internal buffer.
    
    Only sent when the size changes.
    
    Used for raising errors related to exceeding allowed buffer size.

