# Response splitter

[io/http/utils]

Splits a canonical HTTP response into its components: HTTP status, headers, and body.

### Input ports:

* __response__: _`io/http/Response`_

    Receives the canonical HTTP response to be split.



### Output ports:

* __status__: _`io/http/Response`["status"]_



* __headers__: _`io/http/Response`["headers"]_



* __body__: _`io/http/Response`["body"]_



