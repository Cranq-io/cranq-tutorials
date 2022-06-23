---
description: [blockchain/nftport/api v0/utils]
---

# Error detector

Detects errors in the JSON response of NFTPort API endpoints.

Example A)
1. {"response": "OK"}@1 received via `data`
2. No output

Example B)
1. {"response": "NOK", "error": "Invalid creator address."}@1 received via `data`
2. {"error": "Invalid creator address."}@1 sent via `error`

### Input ports:

* __data__: `{"response" :("OK" or "NOK"), "error" :string}`

    Receives parsed response body from an NFTPort API endpoint.


* __status__: `number`

    Receives HTTP status from NFTPort API response.

### Output ports:

* __error__: `{"error" :string}`

