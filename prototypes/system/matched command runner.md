---
description: [system]
---

# Matched command runner

Runs the received command and matches standard output against the specified regular expression.

Sends matched RegEx groups through `groups`.

Sends empty array on no match.

### Input ports:

* __cwd__: `any`

    Receives individual fields for syncing.


* __command__: `string`


* __regex__: `string`

### Output ports:

* __groups__: `string[]`

    Matched RegEx groups

