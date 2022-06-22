# HTML Form POST request dispatcher

[io/http]

Dispatches HTML form POST request and outputs response or error.

Example: 
1. "https://httpbin.org/post"@0 recieved via `URL` 
2.  {}@0 recieved via `headers` 
3. 
{
  "custname": "John Doe",
  "custtel": "1234567890", 
  "custemail": "john.doe@email.doe",  
  "size": "small",
  "topping": ["bacon", "cheese", "onion"]
}@0 recieved via `item` 
4. 200@0 sent via `status`
5. "OK"@0 sent via `body`

### Input ports:

* __URL__: _string_

    Receives the target of the HTML form post.
    
    Example:
    "https://httpbin.org/post"



* __headers__: _{string: string}_

    Receives request headers. 
    
    Example:
    {}



* __form data__: _{string: (string or string[])}_

    Receives the form data to be posted.
    
    Example:
    {
      "custname": "John Doe",
      "custtel": "1234567890", 
      "custemail": "john.doe@email.doe",  
    "size": "small",
    "topping": ["bacon", "cheese", "onion"]
    }



### Output ports:

* __status__: _number_

    Sends HTTP response status code. Indicates whether the request has been  successfully completed.
    
    Example:
    200



* __headers__: _{string: string}_

    Sends HTTP response headers.



* __body__: _string_

    Sends HTTP response message body data.
    
    Example:
    "OK"



* __errors__: _{"error" :string}_

    Sends HTTP response communication error.
    
    
    Example:
    {
      "error": "Error: getaddrinfo ENOTFOUND x.y"
    } 


