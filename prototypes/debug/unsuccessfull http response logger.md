# Unsuccessfull http response logger

[debug]

Logs received 4xx and 5xx responses with a custom message.

### Input ports:

* __response__: _{"status" :number, "headers" :{string: string}, "body" :string}_

    Receives request dispatcher response.
    
    Example: 
    {
     "status": 200, 
     "headers": {}, 
     "body": "OK"
    }



* __message__: _string_

    Receives additional log message.
    
    Example: 
    "unsuccessfull call"



