# First record extractor

[apis/airtable/utils]

Extracts the first record from an AirTable API response.

### Input ports:

* __resp. data__: 
    ```
    {"records" :{"id" :string, "createdTime" :string, "fields" :{string: any}}}
    ```

    JSON body of the record insertion response from AirTable.

### Output ports:

* __record__: 
    ```
    {"records" :{"id" :string, "createdTime" :string, "fields" :{string: any}}}["records"][number]["fields"]
    ```


* __AT record__: 
    ```
    {"records" :{"id" :string, "createdTime" :string, "fields" :{string: any}}}["records"]
    ```

    Record as is sent to / received from the AirTable API.

