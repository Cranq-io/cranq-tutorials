---
description: apis/ga/measurement protocol]
---

# Event params builder

Builds raw "event" parameter set for Google Analytics Measurement Protocol request.

### Input ports:

* __tracking ID__: `any`


* __client ID__: `any`


* __category__: `any`


* __action__: `any`


* __label__: `any`


* __value__: `any`

### Output ports:

* __params__: `{string: ({string: any} and {string: any})}`

    Measurement Protocol parameters for "event" hit type. Key-value pairs, must be serialized to be passed as payload.

