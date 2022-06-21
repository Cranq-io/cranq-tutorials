# Handlebar style template filler

[string]

Substitutes parameters into a template. Parameters are marked by Handlebars style tokens.

Example:

1. "Hello {{subject}}!"@0 is received via `template`
2. {"subject":"world"}@0 is received via params
3. "Hello world!"@0 is sent via `filled`

### Input ports:

* __template__: _string_

    Receives the template string to replace parameters in.
    
    Example:
    "Hello {{subject}}!"



* __params__: _{string: any}_

    Receives the parameters to replace in the template.
    
    Example: 
    {"subject":"world"}



### Output ports:

* __filled__: _string_

    Sends the template string with replaced parameters.
    
    Example:
    "Hello world!"



* __error__: _{"error" :string}_

    Sends error in case any occurs during operation.
    
    Example: 
    {"error": "Some error message"}



