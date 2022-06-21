# JSON listener

[io/http/express]

Starts an express server set up for handling requests and also responding with JSON bodies.

### Input ports:

* __app ID__: _string_

    The id of the express instance.
    
    Example: 
    "my-express-server"



* __port__: _number_

    The port number express should listen to.
    
    Example: 
    3000



### Output ports:

* __done__: _any_



* __error__: _{"error" :string}_

    Sends error information in case the server could not be started or a middleware could not be applied.



