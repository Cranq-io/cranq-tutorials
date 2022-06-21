---
description: [string]
---

# Template filler

Substitutes parameters into a template.

Example:

1. "Hello {subject}!"@0 is received via `template`
2. {"subject":"world"}@0 is received via params
3. "Hello world!"@0 is sent via `filled`

### Input ports:

* __template__: ` string `

    The template to be filled


* __params__: ` {string: any} `

    The actual parameters used for filling the template

### Output ports:

* __filled__: ` string `

    Sends the template filled with the given values from params.

