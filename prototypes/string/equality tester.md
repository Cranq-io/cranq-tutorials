---
description: [string]
---

# Equality tester

Checks if the string received on `a` is equal to string received via `b`.

Example:

1. "foo"@0 is received via `a`
2. "bar"@0 is received via `b`
3. false@0 is sent via `equal`

### Input ports:

* __a__: ` string `

    The first string


* __b__: ` string `

    The second string

### Output ports:

* __equal__: ` boolean `

    Sends true if the two strings are the same, false otherwise.

