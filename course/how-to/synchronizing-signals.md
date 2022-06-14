# Synchronizing signals

<mark style="color:red;">DRAFT</mark>

Synchronizing concurrent signals into [records](../advanced/data-types.md#record) is one of the most common operations in CRANQ. All you need to do to achieve this is - set up a `flow/Syncer` node with the list of field names, and connect the corresponding outputs to the syncer's inputs. The output will be a single record containing each input as a field.
