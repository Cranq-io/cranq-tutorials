# Middlewares applicator

[io/http/express]

Applies multiple Express middlewares.

### Input ports:

* __app ID__: `any`


* __middlewares__: `("text" or "json" or "urlencoded" or "cors")[]`

### Output ports:

* __done__: `any`


* __error__: `{"error" :string}`

    Sends error information in case any of the specified the middlewares could not be applied.

