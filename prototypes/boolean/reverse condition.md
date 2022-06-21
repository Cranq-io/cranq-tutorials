---
description: [boolean]
---

# Reverse condition

Turns binary independent signals into a boolean.

Example A:
1. null@0 is received via `true`
2. true@0 is sent via `boolean`

Example B:
1. "foo"@1 is received via `false`
2. false@1 is sent via `boolean`

### Input ports:

* __to true__: ` any `

    Receives signals to be evaluated to true.


* __to false__: ` any `

    Receives signals to be evaluated to false.

### Output ports:

* __boolean__: ` boolean `

    Sends boolean depending on which input the signal was received through.

