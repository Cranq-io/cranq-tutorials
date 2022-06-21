---
description: [io/http/utils]
---

# Response success detector

Detects whether a HTTP response was successful based on its status code.

### Input ports:

* __status__: ` number `

    HTTP response status code.

### Output ports:

* __success status__: ` number `

    Forwards the status code on success. (1XX, 2XX, 3XX)


* __error status__: ` number `

    Forwards the status code on error. (4XX, 5XX)

