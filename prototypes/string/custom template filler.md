# Custom template filler

[string]

Substitutes parameters into a template. Parameter placeholder's (token) start/end can be customized.

Example:

1. "Hello {#subject#}!"@0 is received via `template`
2. {"subject":"world"}@0 is received via params
3. "{#"@0 is received via `token start`
4. "#}"@0 is received via `token end`
5. "Hello world!"@0 is sent via `filled`

### Input ports:

* __template__: _string_

    Receives the template string to replace parameters in.
    
    Example:
    "Hello {#subject#}!"



* __params__: _{string: any}_

    Receives the parameters to replace in the template.
    
    Example: 
    {"subject":"world"}



* __token start__: _string_

    Receives the string that marks the start of the parameter placeholder (token) within the template.
    
    Example:
    "{#"



* __token end__: _string_

    Receives the string that marks the end of the parameter placholder (token) within the template.
    
    Example:
    "#}"



### Output ports:

* __filled__: _string_

    Sends the template string with replaced parameters.
    
    Example:
    "Hello world!"



* __error__: _{"error" :string}_

    Sends error in case any occurs during operation.
    
    Example: 
    {"error": "Some error message"}



