---
description: [flow/utils]
---

# Burst tester

Sends true on the last signal in bursts of `length` length.

Example:
1. `length` set to 3
2. "A"@0 received via `data`
3. false@0 sent via `is last`
4. "B"@1 received via `data`
5. false@1 sent via `is last`
6. "C"@2 received via `data`
7. true@2 sent via `is last` 

### Input ports:

* __data__: ` any `

    Receives the burst signals.


* __length__: ` number `

    Burst length to be detected.
    
    Can be parameter.

### Output ports:

* __is last__: ` boolean `

    Sends true on the last signal in the burst, false otherwise.

