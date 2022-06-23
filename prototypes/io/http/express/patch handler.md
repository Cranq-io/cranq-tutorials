# PATCH handler

[io/http/express]

Receives PATCH requests on the specified route and dispatches the corresponding response.

Example:
1. "my-express-server"@0 received on `app ID`
2. "/users/"@0 received on `route`
3. a client PATCH request received by express with URL "http://api.mydomain.com/users/2
4. the following signals are sent to other node(s) processing the request
- {
 "accept": "application/json"
}@0 sent on `headers`
- { "age": 29 }@0 sent `body`
5. The following signals are received back from processing nodes and sent out to the client:
- 200@0 on `status`,
- {
    "content-type": "application/json" 
  }@0 on `headers`,
-  { id:2, "name": "John Doe", "age": 29 }@0 on `body`
6. null@0 sent on `done`

### Input ports:

* __app ID__: `string`

    The id of the express instance.
    
    Example: 
    "my-express-server"


* __route__: `(string or string[])`

    Receives the route(s) to handle requests for. Route be specified as exact match (1) or as pattern match (2).
    
    Example:
    1) "/status" will just match "/status"
    2) "/s*s" will match "status", "shoes", etc..


* __status__: `number`

    Receives the HTTP status code to be sent with the response to the client.
    
    Example: 
    200


* __headers__: `{string: string}`

    Receives the HTTP headers to be sent with the response to the client.
    
    Example: 
    {
      "content-type": "application/json"
    }


* __body__: `any`

    Receives the content to send to the client as response body.
    
    Example:
    - "OK"
    - 3.14
    - { "status": "OK" }

### Output ports:

* __headers__: `{string: string}`

    Forwards  the headers of the request to be processed.
    
    Example: 
    {
      "content-type": "application/json"
    }


* __body__: `any`

    Forwards the body of the request to be processed.
    
    Example:
    - "OK"
    - 3.14
    - { "status": "OK" }


* __done__: `any`

    Event triggered when the request has been processed.

