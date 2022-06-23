# URL query appender

[io/http/utils]

Appends a query string based on the query parameters to the specified URLs.

### Input ports:

* __URL__: `string`
    Receives URL without the query component.



* __query params__: `{string: (string or string[])}`


### Output ports:

* __URL + query__: `string`
    Sends URL including the query component.



