# Parser

[number]

Converts a string to number. If the string cannot be converted to number, it will be bounced.

Example:

1. "23.05"@0 is received via `string`
2. 23.05@0 is sent via `number`

### Input ports:

* __string__: _string_

    String input to parse



### Output ports:

* __number__: _number_

    Sends the parsed number if the parsing was successful.



* __bounced__: _string_

    Sends the input data if the parsing has failed.


