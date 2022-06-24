---
description: [testing/reporters/junit]
---

# Reporter

Compiles a JUnit test result report based on incoming assertions.

### Input ports:

* __assertion__: ` any `

    Individual assertion record with properties:
    * type
    * expected
    * actual
    * success
    * description
    * timestamp
    * durations


* __delay__: ` any `

    Maximum allowed delay between assertions in milliseconds.

### Output ports:

* __xml__: ` any `

