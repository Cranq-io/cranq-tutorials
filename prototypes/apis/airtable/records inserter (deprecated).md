# Records inserter (deprecated)

[apis/airtable]

Inserts a list of records into the specified AirTable table.
If the table already contains data, the records are appended.
The input received on parameter `table` must match the target table schema.

For detailed parameter information, see the AirTable API documentation:
https://airtable.com/api/meta

### Input ports:

* __base ID__: _string_

    Receives the AirTable BaseID parameter.



* __table name__: _string_

    Receives the table name to insert the records into.



* __API key__: _string_

    Receives the API key to authenticate with.



* __table__: _{string: any}[]_

    Receives the table of data to insert.



### Output ports:

* __response body__: _typeof `AirtableResponse`_

    Outputs the response from AirTable.


