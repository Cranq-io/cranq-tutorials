# Record deleter

[apis/airtable]

Deletes a single record from an AirTable table.

### Input ports:

* __record ID__: `string`
    Receives the identifier of the record relative to an AirTable table.



* __params__: 
    ```
    {"apiKey" :string, "baseId" :string, "tableName" :string}
    ```



### Output ports:

* __data__: `{"deleted" :boolean, "id" :string}`


* __response__: 
    ```
    {"status" :number, "headers" :{string: any}, "body" :string}
    ```

    Sends the entire response from the AirTable API without modification.



* __error__: `{"error" :string, optional "details" :any}`


