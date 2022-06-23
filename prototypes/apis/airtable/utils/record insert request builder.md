# Record insert request builder

[apis/airtable/utils]

### Input ports:

* __API key__: `string`


* __base ID__: `string`


* __table name__: `string`


* __AT record__: `{"fields" :{string: any}}`

    Record as is sent to / received from the AirTable API.

### Output ports:

* __JSON req.__: 
    ```
    {"method" :("GET" or "POST" or "PUT" or "PATCH" or "DELETE"), "url" :string, "headers" :{string: string}, "data" :{"records" :[{"fields" :{string: any}}]}}
    ```

