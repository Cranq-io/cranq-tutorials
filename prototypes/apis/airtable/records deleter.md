# Records deleter

[apis/airtable]

### Input ports:

* __record IDs__: _string[]_

    Receives list of record identifiers relative to an AirTable table.



* __params__: _{"apiKey" :string, "baseId" :string, "tableName" :string}_



### Output ports:

* __data__: _{"deleted" :boolean, "id" :string[][number]}[]_



* __response__: _{"status" :number, "headers" :{string: any}, "body" :string}_

    Sends the entire response from the AirTable API without modification.



* __error__: _{"error" :string, optional "details" :any}_



