---
description: [data/dictionary]
---

# JSON parser

Parses the JSON string representation of a dictionary.
If the parsing is unsuccessful, the input is forwarded via `bounced`.

Example A:
1. "{\"first\":1,\"third\":3,\"fifth\":5}"@0 received via `json`
2. `parsed` sends { "first": 1, "third": 3, "fifth": 5 }@0

Example B:
1. "malformed"@0 received via `json`
2. `bounced` sends "malformed"@0

More:
https://github.com/Cranq-io/cranq-tutorials/tree/main/reference/2_constructing_data/2_6_serialization

### Input ports:

* __json__: `string`

    Receives the JSON string to parse.
    
    Example:
    "{\"first\":1,\"third\":3,\"fifth\":5}"

### Output ports:

* __parsed__: `{string: any}`

    Sends the parsed dictionary.
    
    Example:
    { "first": 1, "third": 3, "fifth": 5 }


* __bounced__: `string`

    Sends the value of `json`, if the parsing was unsuccessful.


* __error__: `{"error" :string}`

    Sends error information if the operation has failed.
    
    Example: 
    {
      "error": "Error: ENOENT: no such file or directory, open '/home/user1/dir1/foo.txt'"
    }

