# Response error detector

[io/http/utils]

Wraps failed HTTP response into an error, including a message.

Example A
1. `message` set to "Response failed"
2. {"status": 200, "headers": {}, "body": "ABC"}@1 received via `response`
3. null@1 sent via `body`

Example B
1. `message` set to "Response failed"
2. {"status": 400, "headers": {}, "body": {"success": false}}@1 received via `response`
3. {"error": "Response failed", "details": {"success": false}}@1 sent via `error`

### Input ports:

* __response__: _{"status" :number, "headers" :{string: any}, "body" :string}_

    Receives response that might contain an error.



* __error msg__: _string_

    Receives error message to appear in `error`.



### Output ports:

* __body__: _{"status" :number, "headers" :{string: any}, "body" :string}["body"]_



* __error__: _{"error" :string, optional "details" :any}_



