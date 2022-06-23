---
description: apis/airtable]
---

# Record fetcher

Fetches a single record from an AirTable table.

### Input ports:

* __record ID__: `string`

    Receives the identifier of the record relative to an AirTable table.


* __params__: 
    ```
    {"apiKey" :string, "baseId" :string, "tableName" :string}
    ```

### Output ports:

* __record__: `{string: any}`

    Sends the retrieved AirTable record.


* __AT record__: 
    ```
    {"id" :string, "createdTime" :string, "fields" :{string: any}}
    ```

    Sends the retrieved AirTable record, including metadata like row ID, and date & time of creation.


* __response__: 
    ```
    {"status" :number, "headers" :{string: any}, "body" :string}
    ```

    Sends the entire response from the AirTable API without modification.


* __error__: `{"error" :string, optional "details" :any}`

