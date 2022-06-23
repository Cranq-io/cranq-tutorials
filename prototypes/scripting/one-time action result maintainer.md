---
description: [scripting]
---

# One-time action result maintainer

### Input ports:

* __action result__: `boolean`


* __params__: 
    ```
    {"cwd" :string, "result-path" :string, "message" :string}
    ```


* __state__: `any`

    Receives script state.

### Output ports:

* __state (action not started)__: `any`


* __state (action finished)__: `any`

