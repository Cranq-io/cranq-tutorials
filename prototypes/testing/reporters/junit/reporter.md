# Reporter

[testing/reporters/junit]

Compiles a JUnit test result report based on incoming assertions.

### Input ports:

* __assertion__: _any_

    Individual assertion record with properties:
    * type
    * expected
    * actual
    * success
    * description
    * timestamp
    * durations



* __delay__: _any_

    Maximum allowed delay between assertions in milliseconds.



### Output ports:

* __xml__: _any_



