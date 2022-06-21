---
description: [io/http/utils]
---

# Response splitter

Splits a canonical HTTP response into its components: HTTP status, headers, and body.

### Input ports:

* __response__: `` `io/http/Response` ``

    Receives the canonical HTTP response to be split.

### Output ports:

* __status__: `` `io/http/Response`["status"] ``


* __headers__: `` `io/http/Response`["headers"] ``


* __body__: `` `io/http/Response`["body"] ``

