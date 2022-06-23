---
description: string]
---

# Handlebar style template filler

Substitutes parameters into a template. Parameters are marked by Handlebars style tokens.

Example:

1. "Hello {{subject}}!"@0 is received via `template`
2. {"subject":"world"}@0 is received via params
3. "Hello world!"@0 is sent via `filled`

### Input ports:

* __template__: `string`

    Receives the template string to replace parameters in.
    
    Example:
    "Hello {{subject}}!"


* __params__: `{string: any}`

    Receives the parameters to replace in the template.
    
    Example: 
    {"subject":"world"}

### Output ports:

* __filled__: `string`

    Sends the template string with replaced parameters.
    
    Example:
    "Hello world!"


* __error__: `{"error" :string}`

    Sends error in case any occurs during operation.
    
    Example: 
    {"error": "Some error message"}

