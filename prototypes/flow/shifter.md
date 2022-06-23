---
description: [flow]
---

# Shifter

Shifts incoming data back in time by releasing the previously received data on each input. 

Example:
1. "A"@0 received via `data`.
2. "B"@1 received via `data`.
3. "A"@0 sent via `data` (output).

### Input ports:

* __data__: `any`

    Receives signal to be shifted back.

### Output ports:

* __data__: `any`

    Sends previously received signal.

