---
description: scripting/actions]
---

# Express endpoint creator (simplified)

Sets up a route for Express to receive requests on. Routes are expected to follow a format as per Express documentation.

Receiving `state` and `params` inputs initializes the route. Once the route is inialized, incoming requests will be sent out on `request`, and corresponding responses will be expected on `response`, bearing the same tag.

Example:
1. {}@0 received via state
2. {
  "cwd": "express",
  "method": "GET",
  "route": "/status"
}@0 is received via `params`
3. State with route information added is sent via `state`
4. An arbitrary GET request comes in via `request`
5. {"status": 200, "headers": {}, "body": "OK"}@1 is received via `response`
6. The received response is sent to the client.

Links:
* https://expressjs.com/en/guide/routing.html

### Input ports:

* __state__: `any`

    Receives script state.


* __params__: 
    ```
    {"cwd" :string, "method" :("GET" or "POST" or "PUT" or "PATCH" or "DELETE"), "route" :string, "app-id" :string}
    ```

    Receives method and route to match incoming requests against. Also specifies which running Express server instance to use via 'app-id'. The parameter 'app-id' must match the ID of a previously started Express server.


* __response__: 
    ```
    {"status" :number, "headers" :{string: string}, "body" :any}
    ```

    Receives the response for a corresponding request prepared by the logic that connects `request` to `response`.
    
    Properties:
    * 'status' specifies HTTP status code
    * 'headers' list HTTP response headers
    * 'body' specifies the body of the response. Format potentially depends on middlewares.

### Output ports:

* __state__: `any`

    Sends updated script state.


* __request__: 
    ```
    {"baseUrl" :string, "body" :any, "cookies" :any, "hostname" :string, "headers" :{string: string}, "ip" :string, "ips" :string[], "method" :("GET" or "POST" or "PUT" or "PATCH" or "DELETE"), "originalUrl" :string, "params" :{string: string}, "path" :string, "protocol" :("http" or "https"), "query" :{string: any}, "route" :string, "secure" :boolean, "signedCookies" :any, "stale" :boolean, "subdomains" :string[], "xhr" :boolean}
    ```

    Sends incoming requests matching the route and method received via `params`.

