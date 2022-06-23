# Middleware applicator

[io/http/express]

Applies a known middleware to the specified express app.

Accepted middleware identifiers:
* "json"
* "urlencoded"
* "cors"

### Input ports:

* __app ID__: `string`
    Identifies the Express app to apply the middleware on.



* __middleware__: `("text" or "json" or "urlencoded" or "cors")`


### Output ports:

* __done__: `any`


* __app ID__: `string`


* __error__: `{"error" :string}`
    Sends error information in case the middleware could not be applied.



