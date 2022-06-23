# Request timeout handler

[io/http/express/middleware]

Times out a request. If the request reaches the timeout it sends an Request Timeout status as response. 

Examples:

1. `timeout` set to 60000
2. {
  "baseUrl": "",
  "body": "0x495f947276749Ce646f68AC8c248420045cb7b5e,80494307024529346018053650490912529916739680814770830097664395776714464034846",
...
}@0 received via `request`
3. {
  "status": 200,
  "headers": {},
  "body": { }
}@0 received via `response`
4. {
  "status": 200,
  "headers": {},
  "body": { }
}@0 sent via `response`


1. `timeout` set to 30
2. {
  "baseUrl": "",
  "body": "0x495f947276749Ce646f68AC8c248420045cb7b5e,80494307024529346018053650490912529916739680814770830097664395776714464034846",
...
}@0 received via `request`
3. {
  "status": 200,
  "headers": {},
  "body": { }
}@0 received via `response`
4. {
  "status": 408,
  "headers": {},
  "body": "Request Timeout"
}@0 sent via `response`



### Input ports:

* __request__: `any`

    Receives the request.


* __response__: 
    ```
    {"status" :number, "headers" :{string: string}, "body" :string}
    ```

    Receives the response.


* __timeout__: `number`

    Receives the timeout in milliseconds.
    
    Example: 
    300

### Output ports:

* __response__: 
    ```
    {"status" :number, "headers" :{string: string}, "body" :string}
    ```

    Sends response.

