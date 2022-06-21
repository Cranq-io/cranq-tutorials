# Record inserter

[apis/airtable]

Inserts a single records into the specified AirTable table.
The input received on parameter `record` must match the target table schema.

For detailed parameter information, see the AirTable API documentation:
https://airtable.com/api/meta

### Input ports:

* __record__: _{string: any}_

    Receives a single record to be inserted into AirTable.



* __params__: _{"apiKey" :string, "baseId" :string, "tableName" :string}_



### Output ports:

* __record__: _{string: any}_

    Sends the record that was successfully inserted into AirTable.



* __AT record__: _{"id" :string, "createdTime" :string, "fields" :{string: any}}_

    Sends the record that was successfully inserted into AirTable, including metadata like row ID, and date & time of creation.



* __response__: _{"status" :number, "headers" :{string: any}, "body" :string}_

    Sends the entire response from the AirTable API without modification.



* __error__: _{"error" :string, optional "details" :any}_



