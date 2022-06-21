# Status to params mapping creator

[scripting]

Creates mapping to be used with `scripting/Params copier` to map from a previous action's result to a param for a next action.

### Input ports:

* __action params__: _{string: any}_

    Params of the previous action.
    
    Example:
    {
    ...
    "result-path": "foo.bar"
    ...
    }



* __mapping key__: _string_

    The key in params of the next action to receive the result of the specified action from its status.
    
    Example:
    "foobar"



### Output ports:

* __mapping__: _{string: string}_

    The mapping the copy a previous action result from its status to a next action's params.
    
    Example:
    { "foobar": "foo.bar" }



