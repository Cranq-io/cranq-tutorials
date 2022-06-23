---
description: [scripting/actions]
---

# Express server starter (simplified)

Starts an express server on the specified port and with the specified middlewares.

Specifying an 'app-id' allows running multiple express servers at the same time.

Writes the app ID of the started server to state.

Repeatable action.

### Input ports:

* __state__: `any`

    Receives script state.


* __params__: 
    ```
    {"cwd" :string, "app-id" :string, "port" :number, "middlewares" :("json" or "cors" or "urlencoded")[]}
    ```

    Receives:
    * 'cwd' locates directory for persisted state
    * 'app-id' identifies Express server (default: "default")
    * 'port' specifies port to run server on (default: 8080)
    * 'middlewares' lists express middlewares to be activated (default: [])
    
    Example:
    {
      "cwd": "./express",
      "middlewares": ["json"]
    }

### Output ports:

* __state__: `any`

    Sends updates script state.

