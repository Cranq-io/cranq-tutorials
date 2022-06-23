# Error detector

[blockchain/nftport/api v0/utils]

Detects errors in the JSON response of NFTPort API endpoints.

Example A)
1. {"response": "OK"}@1 received via `data`
2. No output

Example B)
1. {"response": "NOK", "error": "Invalid creator address."}@1 received via `data`
2. {"error": "Invalid creator address."}@1 sent via `error`

### Input ports:

* __data__: _{"response" :("OK" or "NOK"), "error" :string}_

    Receives parsed response body from an NFTPort API endpoint.



* __status__: _number_

    Receives HTTP status from NFTPort API response.



### Output ports:

* __error__: _{"error" :string}_



