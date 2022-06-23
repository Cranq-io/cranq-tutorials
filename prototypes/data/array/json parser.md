# JSON parser

[data/array]

Parses a JSON string to  array.

Examples:
A.
1. "[1,2]"@0 recieved via `json`
2. [1,2]@0 sent via `parsed`

B.
1. "{}]"@0 recieved via `json`
2. "{}]"@0 sent via `bounced`

### Input ports:

* __json__: `string`

    Recieves JSON string.
    
    Example:
    "[1,2]"

### Output ports:

* __parsed__: `any[]`

    Sends the parsed array.
    
    Example:
    [1,2]


* __bounced__: `string`

    In case of error during parsing or when the result of the parseisng is not array it sends the `json` input string.
    
    Example:
    "{}]"

