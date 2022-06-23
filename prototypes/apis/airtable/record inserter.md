# Record inserter

[apis/airtable]

Inserts a single records into the specified AirTable table.
The input received on parameter `record` must match the target table schema.

For detailed parameter information, see the AirTable API documentation:
https://airtable.com/api/meta

### Input ports:

* __record__: `{string: any}`

    Receives a single record to be inserted into AirTable.


* __params__: 
    ```
    {"apiKey" :string, "baseId" :string, "tableName" :string}
    ```

### Output ports:

* __record__: `{string: any}`

    Sends the record that was successfully inserted into AirTable.


* __AT record__: 
    ```
    {"id" :string, "createdTime" :string, "fields" :{string: any}}
    ```

    Sends the record that was successfully inserted into AirTable, including metadata like row ID, and date & time of creation.


* __response__: 
    ```
    {"status" :number, "headers" :{string: any}, "body" :string}
    ```

    Sends the entire response from the AirTable API without modification.


* __error__: `{"error" :string, optional "details" :any}`

