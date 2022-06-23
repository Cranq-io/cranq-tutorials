---
description: [scripting]
---

# Starter

Starts a script, by reading the persisted state, or if there is none, initializes an blank state.

Example:
1. {"cwd": "foo"}@0 received via `params`
2. {}@0 sent via `state`

### Input ports:

* __params__: `{"cwd" :string}`

    Receives essential parameters for initializing the state of the script.
    
    Property 'cwd' defaults to "./temp".
    
    Examples:
    * {}
    * {"cwd": "./foo"}

### Output ports:

* __state__: `any`

    Initial state of the program. Sends either the contents of the previously persisted state, or a blank state record.
    
    Examlpe: {}

