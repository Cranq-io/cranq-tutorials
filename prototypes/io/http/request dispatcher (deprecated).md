# Request dispatcher (deprecated)

[io/http]

Use `io/http/Request dispatcher` instead.

Dispatches HTTP request and outputs response or error.

More: https://github.com/Cranq-io/cranq-tutorials/tree/main/http_request

### Input ports:

* __method__: `("GET" or "POST" or "PUT" or "PATCH" or "DELETE")`
    Receives http method. Indicates the desired action to be performed for a given target or resource.
    
    Example:
    "GET"



* __URL__: `string`
    Receives the target of the HTTP request. Also called "resource" 
    
    Example:
    "https://jsonplaceholder.typicode.com/todos/1"



* __headers__: `{string: string}`
    Receives request headers. It is  used to describe a resource, or the behavior of the server or the client.
    
    Example:
    {
      "content-type": "application/json; charset=utf-8"
    }



* __body__: `string`
    Receives the http request body. Some requests send data to the server in order to update it. In case of GET or DELETE request the body should be empty (will be ignored).
    
    Example:
    ""



### Output ports:

* __status__: `number`
    Sends http response status code. Indicates whether the request has been  successfully completed.
    
    Example:
    200



* __headers__: `{string: string}`
    Sends http response headers.
    
    Example:
    {
    "content-type": "application/json; charset=utf-8",
    "cache-control":"max-age=43200"
    }
    



* __body__: `string`
    Sends http response message body data.
    
    Example:
    "{\"userId\": 1, \"id\": 1, \"title\": \"delectus aut autem\",  \"completed\": false
    }"



* __error__: `{"error" :string}`
    Sends http response communication error.
    
    
    Example:
    {
      "error": "Error: getaddrinfo ENOTFOUND x.y"
    } 



* __response__: 
    ```
    {"status" :number, "headers" :{string: any}, "body" :string}
    ```



