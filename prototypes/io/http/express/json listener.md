---
description: [io/http/express]
---

# JSON listener

Starts an express server set up for handling requests and also responding with JSON bodies.

### Input ports:

* __app ID__: ` string `

    The id of the express instance.
    
    Example: 
    "my-express-server"


* __port__: ` number `

    The port number express should listen to.
    
    Example: 
    3000

### Output ports:

* __done__: ` any `


* __error__: ` {"error" :string} `

    Sends error information in case the server could not be started or a middleware could not be applied.

