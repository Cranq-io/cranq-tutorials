# Express

[io/http/express]

Core interface to Express.js. Use higher level nodes to interact with Express.

### Input ports:

* __action__: _{"id" :string, "type" :string, "options" :{string: any}}_

    Receives the parameters of the action to execute.
    
    Example: 
    {
      "id": "my-express-server",
      "type": "listen",
      "options": {
        "port": 3000
      }
    }



* __response__: _{"status" :number, "headers" :{string: string}, "body" :any}_

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

* __request__: _{"baseUrl" :string, "body" :any, "cookies" :any, "hostname" :string, "headers" :{string: string}, "ip" :string, "ips" :string[], "method" :("GET" or "POST" or "PUT" or "PATCH" or "DELETE"), "originalUrl" :string, "params" :{string: string}, "path" :string, "protocol" :("http" or "https"), "query" :{string: any}, "route" :string, "secure" :boolean, "signedCookies" :any, "stale" :boolean, "subdomains" :string[], "xhr" :boolean}_

    Sends the request processed by  defined handlers. Can be used to post-process the request.



* __done__: _null_

    Event triggered when the specified action has been executed.



* __error__: _{"error" :string}_

    Sends error information in case the specified action could not be successfully executed.
    
    Example:
    {
      "error": "Error: listen EADDRINUSE: address already in use :::3000"
    }


