# Action finished tester

[scripting]

Tests whether there's a result recorded on the specified result path of the state.

### Input ports:

* __state__: `any`
    Receives script state.



* __result path__: `(string or number)[]`
    Locates an action result in the state.



### Output ports:

* __on finished__: `any`
    Forwards state when result path exists.



* __on not started__: `any`
    Forwards state when result path does not exist.



