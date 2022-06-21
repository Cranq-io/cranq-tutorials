# JSON request dispatcher

[io/http]

Dispatches HTTP request, expects response as JSON, parses it and outputs it as data. Outputs error if failed.

More: https://github.com/Cranq-io/cranq-tutorials/tree/main/http_request

### Input ports:

* __JSON req.__: _{"method" :("GET" or "POST" or "PUT" or "PATCH" or "DELETE"), "url" :string, "headers" :{string: string}, optional "data" :any}_

    Receives request with JSON body.



### Output ports:

* __data__: _any_

    Sends HTTP response message body as data.
    
    Example:
    {
      "userId": 1, 
      "id": 1, 
      "title": "delectus aut autem",  
      "completed": false
    }"



* __response__: _{"status" :number, "headers" :{string: any}, "body" :string}_

    Sends original response.



* __error__: _{"error" :string}_



