---
description: [io/http/utils]
---

# Bearer token checker

Checks for the presence of the specified bearer token in the submitted request headers. Forwards request body only when found.

### Input ports:

* __bearer token__: ` string `

    Receives the bearer token to be verified.


* __request__: ` {"headers" :{string: string}, "body" :string} `

    Receives the request to be authorized.

### Output ports:

* __request__: ` {"headers" :{string: string}, "body" :string} `


* __error__: ` {"error" :"incorrect bearer token"} `

