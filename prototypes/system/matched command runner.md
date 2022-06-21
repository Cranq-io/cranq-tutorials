# Matched command runner

[system]

Runs the received command and matches standard output against the specified regular expression.

Sends matched RegEx groups through `groups`.

Sends empty array on no match.

### Input ports:

* __cwd__: _any_

    Receives individual fields for syncing.



* __command__: _string_



* __regex__: _string_



### Output ports:

* __groups__: _string[]_

    Matched RegEx groups



