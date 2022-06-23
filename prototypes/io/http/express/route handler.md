---
description: io/http/express]
---

# Route handler

Receives requests on the specified route and dispatches the corresponding response.
You may also consider method specific route handlers for easier use.

Example:
1. "my-express-server"@0 received on `app ID`
2. "GET"@0 received on `method`
3. "/status/"@0 received on `route`
4. a client GET request received by express with URL "http://api.mydomain.com/status"
5. {
"body": "", 
"hostname": "api.mydomain.com", 
"method": "GET", 
"path": "/status", 
"protocol": "http", 
}@0 sent on `request`to other node for processing
6. {
  "status": 200,
  "headers": {
    "content-type": "application/json" 
  },
  "body": { status: "OK" } 
}@0 received back on `response` from processing nodes and sent out to the client
7.
- null@0 sent on `done`
- "my-express-server"@0 sent on `app ID`

### Input ports:

* __app ID__: `string`

    The id of the express instance.
    
    Example: 
    "my-express-server"


* __method__: `("GET" or "POST" or "PUT" or "PATCH" or "DELETE")`

    Receives the method to handle request for. 
    
    Example:
    "GET"


* __route__: `(string or string[])`

    Receives the route(s) to handle requests for. Route be specified as exact match (1) or as pattern match (2).
    
    Example:
    1) "/status" will just match "/status"
    2) "/s*s" will match "status", "shoes", etc..
    


* __response__: 
    ```
    {"status" :number, "headers" :{string: string}, "body" :any}
    ```

    Receives the response to be sent out to the client.
    
    Example:
    {
      "status": 200,
      "headers": {
        "content-type": "application/json" 
      },
      "body": "Done"
    }

### Output ports:

* __request__: 
    ```
    {"baseUrl" :string, "body" :any, "cookies" :any, "hostname" :string, "headers" :{string: string}, "ip" :string, "ips" :string[], "method" :("GET" or "POST" or "PUT" or "PATCH" or "DELETE"), "originalUrl" :string, "params" :{string: string}, "path" :string, "protocol" :("http" or "https"), "query" :{string: any}, "route" :string, "secure" :boolean, "signedCookies" :any, "stale" :boolean, "subdomains" :string[], "xhr" :boolean}
    ```

    Forwards the request to be processed.


* __done__: `null`

    Event triggered when the specified action has been executed.


* __app ID__: `string`

    The id of the express instance the action was executed on. Emitted when the action was executed.
    To be used when chaining multiple actions on the same express instance.
    
    Example: 
    "my-express-server"


* __error__: `{"error" :string}`

    Sends error information in case the request could not be handled.

