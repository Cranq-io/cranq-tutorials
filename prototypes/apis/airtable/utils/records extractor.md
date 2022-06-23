# Records extractor

[apis/airtable/utils]

Extracts all records from an AirTable API response.

### Input ports:

* __resp. data__: 
    ```
    {"records" :{"id" :string, "createdTime" :string, "fields" :{string: any}}}
    ```

    JSON body of the record insertion response from AirTable.



### Output ports:

* __records__: 
    ```
    {"records" :{"id" :string, "createdTime" :string, "fields" :{string: any}}}["records"][number]["fields"][]
    ```



* __AT records__: 
    ```
    {"records" :{"id" :string, "createdTime" :string, "fields" :{string: any}}}["records"][]
    ```

    Record as are sent to / received from the AirTable API.



