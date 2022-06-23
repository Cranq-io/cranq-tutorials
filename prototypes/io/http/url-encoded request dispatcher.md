---
description: io/http]
---

# URL-encoded request dispatcher

Dispatches HTTP request with an URL encoded body, expects response as JSON, parses it and outputs it as data. Outputs error if failed.

### Input ports:

* __URL-enc. req.__: 
    ```
    {"method" :string, "url" :string, "headers" :{string: string}, "data" :{string: (string or string[])}}
    ```

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
    {"status" :number, "headers" :{string: string}, "body" :string}
    ```

    Sends original response.


* __error__: `{"error" :string}`

