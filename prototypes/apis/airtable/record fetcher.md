# Record fetcher

[apis/airtable]

Fetches a single record from an AirTable table.

### Input ports:

* __record ID__: _string_

    Receives the identifier of the record relative to an AirTable table.



* __params__: _{"apiKey" :string, "baseId" :string, "tableName" :string}_



### Output ports:

* __record__: _{string: any}_

    Sends the retrieved AirTable record.



* __AT record__: _{"id" :string, "createdTime" :string, "fields" :{string: any}}_

    Sends the retrieved AirTable record, including metadata like row ID, and date & time of creation.



* __response__: _{"status" :number, "headers" :{string: any}, "body" :string}_

    Sends the entire response from the AirTable API without modification.



* __error__: _{"error" :string, optional "details" :any}_



