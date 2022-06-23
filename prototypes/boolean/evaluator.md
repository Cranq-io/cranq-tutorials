---
description: [boolean]
---

# Evaluator

Determines whether the input is truthy or falsy.

Example A (for truthy):

1. 23@0 is received via `value`
2. true@0 is sent via `boolean`

Example B (for falsy):
1. null@0 is received via `value`
2. false@0 is sent via `boolean`

### Input ports:

* __value__: `any`

    Data to be evaulated as boolean

### Output ports:

* __boolean__: `boolean`

    The value evaulated as boolean.

