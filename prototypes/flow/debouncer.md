---
description: [flow]
---

# Debouncer

Debounces signals received through `data`.

Example:
1. `delay` is set to 1000.
2. "a"@0 received via `data`
3. waiting 0.5s (500ms)
4. "b"@1 received via `data`
5. waiting 1.1s (1100ms)
6. "b"@1 sent via `data` (output)

### Input ports:

* __data__: ` any `

    Receives signal to be debounced.


* __delay__: ` number `

    Minimum delay in milliseconds between last signal received through `data` (input) and sent through `data` (output).
    
    Must be set as a parameter.

### Output ports:

* __data__: ` any `

    Sends the debounced signal.

