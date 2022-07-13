# Port

The port is where nodes receive and send data. Data enters nodes through _input_ ports, either as [signals](broken-reference), or [parameters](broken-reference), then signals (and signals only) leave via _output_ ports.

Ports have [data types](broken-reference) associated with them, which helps determining whether a parameter or a connected port is compatible. Connecting incompatible ports may lead to unexpected behavior (bugs).

Data types in CRANQ must be compatible with [JSON](https://en.wikipedia.org/wiki/JSON), including strings (text), numbers, boolean (true / false), null (special value), arrays (lists), and dictionaries (records).
