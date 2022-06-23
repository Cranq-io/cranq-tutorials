# Records deleter

[apis/airtable]

### Input ports:

* __record IDs__: `string[]`
    Receives list of record identifiers relative to an AirTable table.



* __params__: 
    ```
    {"apiKey" :string, "baseId" :string, "tableName" :string}
    ```



### Output ports:

* __data__: `{"deleted" :boolean, "id" :string[][number]}[]`


* __response__: 
    ```
    {"status" :number, "headers" :{string: any}, "body" :string}
    ```

    Sends the entire response from the AirTable API without modification.



* __error__: `{"error" :string, optional "details" :any}`


