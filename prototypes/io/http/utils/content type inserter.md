# Content type inserter

[io/http/utils]

Inserts content type into a HTTP request header.

Example:
1. {}@0 received via `headers`
2. "application/json"@0 received on `content type`
3. {"Content-Type": "application/json"}@0 sent via `headers`

### Input ports:

* __headers__: `{string: string}`

    Recieves request headers. It is  used to describe a resource, or the behavior of the server or the client.
    
    Example:
    {
      "content-type": "application/json; charset=utf-8"
    }


* __content type__: `string`

    Receives the content type to be inserted into the headers.
    
    Examples:
    * "application/json"
    * "text/plain"
    
    

### Output ports:

* __headers__: `{string: string}`

    Sends the received request headers with the content type header added to it.
    
    Example:
    {
      "Content-Type": "application/json"
    }

