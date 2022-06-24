---
description: [scripting/actions]
---

# Matched command runner

### Input ports:

* __state__: ` any `

    Receives script state.


* __params__: 
    ```
    {"cwd" :string, "result-path" :string, "message" :string, "command" :string, "regex" :string}
    ```

### Output ports:

* __state__: ` any `

    Sends updated script state.

