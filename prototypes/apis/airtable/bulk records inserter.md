# Bulk records inserter

[apis/airtable]

Inserts multiple records into the specified AirTable table.
The input received on parameter `records` must match the target table schema.

Sends records to the AirTable API in batches of 10.

For detailed parameter information, see the AirTable API documentation:
https://airtable.com/api/meta

### Input ports:

* __records__: `{string: any}[]`
    Receives arbitrary number of records to be inserted into AirTable.



* __params__: 
    ```
    {"apiKey" :string, "baseId" :string, "tableName" :string}
    ```



### Output ports:

* __records__: `{string: any}[]`
    Sends records that were successfully inserted into AirTable.



* __AT records__: 
    ```
    {"id" :string, "createdTime" :string, "fields" :{string: any}[][number]}[]
    ```

    Sends records that were successfully inserted into AirTable, including metadata like row ID, and date & time of creation.



* __responses__: 
    ```
    {"status" :number, "headers" :{string: any}, "body" :string}[]
    ```

    Sends the entire response from the AirTable API without modification.



* __error__: `{"error" :string, optional "details" :any}`


