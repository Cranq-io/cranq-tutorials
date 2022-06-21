# Records to AirTable records converter

[apis/airtable/utils]

Converts plain list of records (table) to a list of AirTable records.

### Input ports:

* __records__: _{string: any}[]_



### Output ports:

* __AT records__: _{"fields" :{string: any}[][number]}[]_

    Records as are sent to / received from the AirTable API.



