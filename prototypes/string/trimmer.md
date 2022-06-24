---
description: [string]
---

# Trimmer

Removes whitespace from both ends of  `string` input.

Example:
1. "  foo"@0 received via `string`
2. "foo"@0 sent via `trimmed`

### Input ports:

* __string__: ` string `

    Receives string to be trimmed.
    
    Example:
    "  foo"

### Output ports:

* __trimmed__: ` string `

    Sends trimmed string.
    
    Example
    "foo"

