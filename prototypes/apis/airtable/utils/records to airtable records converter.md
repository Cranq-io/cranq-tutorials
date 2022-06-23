---
description: [apis/airtable/utils]
---

# Records to AirTable records converter

Converts plain list of records (table) to a list of AirTable records.

### Input ports:

* __records__: `{string: any}[]`

### Output ports:

* __AT records__: `{"fields" :{string: any}[][number]}[]`

    Records as are sent to / received from the AirTable API.

