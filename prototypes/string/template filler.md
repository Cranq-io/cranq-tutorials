# Template filler

[string]

Substitutes parameters into a template.

Example:

1. "Hello {subject}!"@0 is received via `template`
2. {"subject":"world"}@0 is received via params
3. "Hello world!"@0 is sent via `filled`

### Input ports:

* __template__: _string_

    The template to be filled



* __params__: _{string: any}_

    The actual parameters used for filling the template



### Output ports:

* __filled__: _string_

    Sends the template filled with the given values from params.



