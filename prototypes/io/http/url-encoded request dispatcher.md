# URL-encoded request dispatcher

[io/http]

Dispatches HTTP request with an URL encoded body, expects response as JSON, parses it and outputs it as data. Outputs error if failed.

### Input ports:

* __URL-enc. req.__: _{"method" :string, "url" :string, "headers" :{string: string}, "data" :{string: (string or string[])}}_



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



* __response__: _{"status" :number, "headers" :{string: string}, "body" :string}_

    Sends original response.



* __error__: _{"error" :string}_



