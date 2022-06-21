# Type tester

[number]

Tells whether the received value on `data` is a number.

Example (not a number):

1. "some string"@0 is received via `data`
2. false@0 is sent via `is number`

Example (receives a number):

1. 23.23@0 is received via `data`
2. true@0 is sent via `is number`

### Input ports:

* __data__: _any_

    the value to be tested.



### Output ports:

* __is number__: _boolean_

    Sends true if the data is a number, false otherwise.



