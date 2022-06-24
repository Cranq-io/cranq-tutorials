---
description: [flow]
---

# Forwarder (double)

Forwards both received signals in the order of the names of the ports.

Used for two purposes:
* Ensuring that any of a node's inputs may receive signals or be set as parameter.
* Ensuring the order in which signals are sent.

Example a) param vs. signal:
1. `2`(input) set to "B"
2. "A"@0 received via `1` (input)
3. "A"@0 sent via `1` (output)
4. "B"@0 sent via `2` (output)

Example b) signal order:
1. "B"@0 received via `2` (input)
2. "A"@0 received via `1` (input)
3. "A"@0 sent via `1` (output)
4. "B"@0 sent via `2` (output)

### Input ports:

* __1__: ` any `

    Receives signal or takes parameter to be sent out first.


* __2__: ` any `

    Receives signal or takes parameter to be sent out second.

### Output ports:

* __1__: ` any `

    Forwards signal received via `1` (input).


* __2__: ` any `

    Forwards signal received via `2` (input). Does not send before `1` (output).

