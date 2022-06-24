---
description: [scripting/actions]
---

# Dotenv appender

### Input ports:

* __state__: ` any `

    Receives script state.


* __params__: 
    ```
    {"cwd" :string, "result-path" :string, "message" :string, "name" :string, "value" :string, "append" :boolean}
    ```

### Output ports:

* __state__: ` any `

    Sends updated script state.

