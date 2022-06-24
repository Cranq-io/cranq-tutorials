---
description: [scripting/actions]
---

# Express route creator

Sets up an API endpoint using Express. An express server must be started in the script before the flow gets to this one.

See `scripting/actions/Express server starter`.

### Input ports:

* __state__: ` any `

    Receives script state.


* __params__: 
    ```
    {"cwd" :string, "result-path" :string, "message" :string, "method" :("GET" or "POST" or "PUT" or "PATCH" or "DELETE"), "route" :string, "app-id" :string}
    ```


* __response__: 
    ```
    {"status" :number, "headers" :{string: string}, "body" :any}
    ```

### Output ports:

* __state__: ` any `

    Sends updated script state.


* __request__: 
    ```
    {"baseUrl" :string, "body" :any, "cookies" :any, "hostname" :string, "headers" :{string: string}, "ip" :string, "ips" :string[], "method" :("GET" or "POST" or "PUT" or "PATCH" or "DELETE"), "originalUrl" :string, "params" :{string: string}, "path" :string, "protocol" :("http" or "https"), "query" :{string: any}, "route" :string, "secure" :boolean, "signedCookies" :any, "stale" :boolean, "subdomains" :string[], "xhr" :boolean}
    ```

