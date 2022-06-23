---
description: [io/http]
---

# Request dispatcher

Dispatches HTTP request and outputs response or error.

More: https://github.com/Cranq-io/cranq-tutorials/tree/main/http_request

### Input ports:

* __params__: 
    ```
    {"method" :("GET" or "POST" or "PUT" or "PATCH" or "DELETE"), "url" :string, "headers" :{string: string}, optional "body" :string}
    ```

    Receives parameters of the HTTP request.
    
    Example:
    
    {
      "verb":"GET,
      "url": "https://jsonplaceholder.typicode.com/todos/1",
      "headers": {
        "content-type": 
      "application/json; charset=utf-8"
      }
    }

### Output ports:

* __response__: 
    ```
    {"status" :number, "headers" :{string: string}, "body" :string}
    ```

    Sends HTTP response object.
    
    Example:
    
    {
      "status": 200,
      "headers": {
        "content-type": "application/json; charset=utf-8",
        "cache-control": "max-age=43200"
      },
      "body": "{\"userId\": 1, \"id\": 1, \"title\": \"delectus aut autem\",  \"completed\": false
    }"
    }


* __error__: `{"error" :string}`

    Sends error on failing to send or receive the request.
    
    Example:
    
    {
      "error": "Error: getaddrinfo ENOTFOUND x.y"
    } 

