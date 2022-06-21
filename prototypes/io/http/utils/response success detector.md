# Response success detector

[io/http/utils]

Detects whether a HTTP response was successful based on its status code.

### Input ports:

* __status__: _number_

    HTTP response status code.



### Output ports:

* __success status__: _number_

    Forwards the status code on success. (1XX, 2XX, 3XX)



* __error status__: _number_

    Forwards the status code on error. (4XX, 5XX)



