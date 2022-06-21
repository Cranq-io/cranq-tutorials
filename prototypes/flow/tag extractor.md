# Tag extractor

[flow]

Maps the signal received via `data` to its tag.

Example:
1. "A"@0 received via `data`
2. "0"@0 sent via `tag`

### Input ports:

* __data__: _any_

    Receives the signal to extract the tag from.



### Output ports:

* __tag__: _string_

    Sends the extracted tag.



