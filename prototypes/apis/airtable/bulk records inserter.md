# Bulk records inserter

[apis/airtable]

Inserts multiple records into the specified AirTable table.
The input received on parameter `records` must match the target table schema.

Sends records to the AirTable API in batches of 10.

For detailed parameter information, see the AirTable API documentation:
https://airtable.com/api/meta

### Input ports:

* __records__: _{string: any}[]_

    Receives arbitrary number of records to be inserted into AirTable.



* __params__: _{"apiKey" :string, "baseId" :string, "tableName" :string}_



### Output ports:

* __records__: _{string: any}[]_

    Sends records that were successfully inserted into AirTable.



* __AT records__: _{"id" :string, "createdTime" :string, "fields" :{string: any}[][number]}[]_

    Sends records that were successfully inserted into AirTable, including metadata like row ID, and date & time of creation.



* __responses__: _{"status" :number, "headers" :{string: any}, "body" :string}[]_

    Sends the entire response from the AirTable API without modification.



* __error__: _{"error" :string, optional "details" :any}_



