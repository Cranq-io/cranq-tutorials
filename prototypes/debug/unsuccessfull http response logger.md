---
description: [debug]
---

# Unsuccessfull http response logger

Logs received 4xx and 5xx responses with a custom message.

### Input ports:

* __response__: 
    ```
    {"status" :number, "headers" :{string: string}, "body" :string}
    ```

    Receives request dispatcher response.
    
    Example: 
    {
     "status": 200, 
     "headers": {}, 
     "body": "OK"
    }


* __message__: `string`

    Receives additional log message.
    
    Example: 
    "unsuccessfull call"

