---
description: io/http/express]
---

# Listener

Sets up the specified Express server to listen on the specified port.

Example:
1. "my-express-server"@0 received on `app ID`
2. 3000@0 received on `port`
3. Express server is started to listen on http//localhost:3000
4/a. In case of success
-  null@0 sent on `done`
- "my-express-server"@0 sent on `app iD`
4/b. In case of failure
-  {
  "code": "EADDRINUSE",
  "errno": -98,
  "syscall": "listen",
  "address": "::",
  "port": 3000
}@0 sent on `error`


### Input ports:

* __app ID__: `string`

    The id of the express instance.
    
    Example: 
    "my-express-server"


* __port__: `number`

    The port number express should listen to.
    
    Example: 
    3000

### Output ports:

* __done__: `null`

    Event triggered when the action has been executed.


* __error__: `{"error" :string}`

    Sends error information in case the specified action could not be successfully executed.
    
    Example:
    {
      "code": "EADDRINUSE",
      "errno": -98,
      "syscall": "listen",
      "address": "::",
      "port": 3000
    }


* __app ID__: `string`

    DEPRECATED
    
    The id of the express instance the action was executed on. Emitted when the action was executed.
    To be used when chaining multiple actions on the same express instance.
    
    Example: 
    "my-express-server"

