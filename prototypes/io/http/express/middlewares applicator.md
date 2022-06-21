# Middlewares applicator

[io/http/express]

Applies multiple Express middlewares.

### Input ports:

* __app ID__: _any_



* __middlewares__: _("text" or "json" or "urlencoded" or "cors")[]_



### Output ports:

* __done__: _any_



* __error__: _{"error" :string}_

    Sends error information in case any of the specified the middlewares could not be applied.



