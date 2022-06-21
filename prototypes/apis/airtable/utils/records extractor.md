# Records extractor

[apis/airtable/utils]

Extracts all records from an AirTable API response.

### Input ports:

* __resp. data__: _{"records" :{"id" :string, "createdTime" :string, "fields" :{string: any}}}_

    JSON body of the record insertion response from AirTable.



### Output ports:

* __records__: _{"records" :{"id" :string, "createdTime" :string, "fields" :{string: any}}}["records"][number]["fields"][]_



* __AT records__: _{"records" :{"id" :string, "createdTime" :string, "fields" :{string: any}}}["records"][]_

    Record as are sent to / received from the AirTable API.



