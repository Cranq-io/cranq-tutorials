---
description: blockchain/ethereum/actions]
---

# Contract verifier

### Input ports:

* __state__: `any`

    Receives script state.


* __params__: 
    ```
    {"contract-address" :string, "cwd" :string, "result-path" :string, "message" :string}
    ```

### Output ports:

* __state__: `any`

    Sends updated script state.

