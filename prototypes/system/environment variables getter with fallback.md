# Environment variables getter with fallback

[system]

Gets a list variable from either the system environment by name or the provided fallback default values. Sends a dictionary with a dictionary of names that have been resolved either way.

Example: 
1. `variable names` receives a list of environment variable names ["Var1", "Var2"]@0
2. `default values` receives optional default values { "var1": "value1" }@0

### Input ports:

* __variable names__: _string[]_

    Receives a list of variable names to be resolved from the environment.
    
    Example:
    ["Var1", "Var2"]



* __default values__: _{string: string}_

    Receives optional default values for undefined environment variables.
    
    Example:
    { "var1": "value1" }



### Output ports:

* __resolved variables__: _{string: string}_

    Sends the dictionary of resolved environment variables as a name:value dictionary.
    
    Contains the environment value if found, otherwise the specified default value if any.
    
    
    Example:
    {
      "V1": "value 1",
      "V2": "default value 2"
    }



