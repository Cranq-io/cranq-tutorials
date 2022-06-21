# Record insert request builder

[apis/airtable/utils]

### Input ports:

* __API key__: _string_



* __base ID__: _string_



* __table name__: _string_



* __AT record__: _{"fields" :{string: any}}_

    Record as is sent to / received from the AirTable API.



### Output ports:

* __JSON req.__: _{"method" :("GET" or "POST" or "PUT" or "PATCH" or "DELETE"), "url" :string, "headers" :{string: string}, "data" :{"records" :[{"fields" :{string: any}}]}}_



