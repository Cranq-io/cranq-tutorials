---
description: data/dictionary]
---

# JSON serializer

Serializes a dictionary to its JSON string representation.

Example A:
1. { "first": 1, "third": 3, "fifth": 5 }@0 received via `dict`
2. `json` sends "{\"first\":1,\"third\":3,\"fifth\":5}"@0

More:
https://github.com/Cranq-io/cranq-tutorials/tree/main/reference/2_constructing_data/2_6_serialization

### Input ports:

* __dict__: `any`

    Receives the dictionary to serialize.
    
    Example:
    { "first": 1, "third": 3, "fifth": 5 }

### Output ports:

* __json__: `any`

    Sends the JSON string representation of the provided dictionary.
    
    Example:
    "{\"first\":1,\"third\":3,\"fifth\":5}"

