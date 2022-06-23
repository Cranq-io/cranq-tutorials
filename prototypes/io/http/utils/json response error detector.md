---
description: [io/http/utils]
---

# JSON response error detector

Wraps failed HTTP response into an error, including a message.

Example A
1. `message` set to "Response failed"
2. {"status": 200, "headers": {}, "body": "null"}@1 received via `response`
3. null@1 sent via `data`

Example B
1. `message` set to "Response failed"
2. {"status": 400, "headers": {}, "body": {"success": false}}@1 received via `response`
3. {"error": "Response failed", "details": {"success": false}}@1 sent via `error`

### Input ports:

* __response__: 
    ```
    {"status" :number, "headers" :{string: any}, "body" :string}
    ```

    Receives JSON response that might contain an error.


* __error msg__: `string`

    Receives error message to appear in `error`.

### Output ports:

* __data__: `any`

    Sends response data, when the response was successful.


* __error__: `{"error" :string, optional "details" :any}`

