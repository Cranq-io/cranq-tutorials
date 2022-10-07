# Tag

The tag identifies the _origin_ of a signal.

The concept of the tag is the secret sauce in CRANQ's flavor of [dataflow programming](dataflow-programming.md). Its primary purpose is synchronization of signals that "go together". For instance, in the case of a node that adds two numbers together (eg. `number/Adder`), the two independent input signals must be recognized as a pair, so the node can calculate their sum. In cases like that, the output inherits the tag of the correspondig inputs.

![Matching tags on addition](<../../.gitbook/assets/Screenshot 2022-07-18 at 15.59.04.png>)

:wrench: The tag serves other purposes, eg. indicating signal multiplicity at runtime. Typically, nodes that iterate over an array or dictionary, emit signals for each iteration with unique tags, so that synchronization of those signals remain consistent.

Any given port, in optimal circumstances, would not receive or send a signal with the same tag more than once during the program's lifecycle. When they do, it's usually a sign of potential bugs.

{% hint style="info" %}
In most cases nodes send their output with the input signal's original tag.
{% endhint %}
