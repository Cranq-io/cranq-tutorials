---
description: string]
---

# URI component encoder

URI component-encodes the received string.

Example:
1. "hello world"@1 received via `string`
2. "hello%20world"@1 sent via `encoded`

### Input ports:

* __string__: `any`

    Receives a string to be URI component-encoded.

### Output ports:

* __encoded__: `string`

    Sends the URI component-encoded string.

