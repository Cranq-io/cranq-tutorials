# First record extractor

[apis/airtable/utils]

Extracts the first record from an AirTable API response.

### Input ports:

* __resp. data__: _{"records" :{"id" :string, "createdTime" :string, "fields" :{string: any}}}_

    JSON body of the record insertion response from AirTable.



### Output ports:

* __record__: _{"records" :{"id" :string, "createdTime" :string, "fields" :{string: any}}}["records"][number]["fields"]_



* __AT record__: _{"records" :{"id" :string, "createdTime" :string, "fields" :{string: any}}}["records"]_

    Record as is sent to / received from the AirTable API.



