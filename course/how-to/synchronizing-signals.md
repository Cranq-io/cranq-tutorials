# Synchronizing signals

[Signals](../basics/103/#signal) in CRANQ are assumed to be asynchronous by default. It does not matter in what (chronological) order a node receives its inputs, as long as they bear the same [tag](../basics/103/#tag). If they do, they can be treated as a single signal onwards.

In any CRANQ program, signals are zipping around all the time, so synchronizing concurrent ones into [records](../advanced/data-types.md#record) is one of the most common operations.&#x20;

All you need to do is, set up a `flow/Syncer` node with the list of field names, and connect the corresponding outputs to the syncer's inputs. The output will be a single record containing each input as a field by the associated name.

\[image]
