# Middleware applicator

[io/http/express]

Applies a known middleware to the specified express app.

Accepted middleware identifiers:
* "json"
* "urlencoded"
* "cors"

### Input ports:

* __app ID__: _string_

    Identifies the Express app to apply the middleware on.



* __middleware__: _("text" or "json" or "urlencoded" or "cors")_



### Output ports:

* __done__: _any_



* __app ID__: _string_



* __error__: _{"error" :string}_

    Sends error information in case the middleware could not be applied.



