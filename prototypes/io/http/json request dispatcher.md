---
description: io/http]
---

# JSON request dispatcher

Dispatches HTTP request, expects response as JSON, parses it and outputs it as data. Outputs error if failed.

More: https://github.com/Cranq-io/cranq-tutorials/tree/main/http_request

### Input ports:

* __JSON req.__: 
    ```
    {"method" :("GET" or "POST" or "PUT" or "PATCH" or "DELETE"), "url" :string, "headers" :{string: string}, optional "data" :any}
    ```

    Receives request with JSON body.

### Output ports:

* __data__: `any`

    Sends HTTP response message body as data.
    
    Example:
    {
      "userId": 1, 
      "id": 1, 
      "title": "delectus aut autem",  
      "completed": false
    }"


* __response__: 
    ```
    {"status" :number, "headers" :{string: any}, "body" :string}
    ```

    Sends original response.


* __error__: `{"error" :string}`

