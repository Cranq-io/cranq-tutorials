# Connection

A connection _transmits_ [signals](signal.md) between [ports](port.md). For connections between _sibling nodes_, an output port is always connected to one or more input ports. For connections between _parent and child_, connections go either from the parents' inputs to children's inputs, or children's outputs to the parent's outputs.

Connections going from the parent's input port to children's input ports _propagate_ the [parameter](parameter.md) set on the parent's port to the connected ports.

* When transmitting, connected output ports receive the signals immediately as they appear on the sender's output port.
* When propagating parameters, inherited parameter values get set on connected input ports as you enter them.

![Connection between nodes](<../../.gitbook/assets/Screenshot 2022-07-18 at 13.07.18.png>) ![Connection from parent to child](<../../.gitbook/assets/Screenshot 2022-07-18 at 13.07.18 copy.png>)

## One-to-many and many-to-one

When a single output port has multiple inputs connected, all connected input ports will receive the same signal that was sent by the output.

Similarly, when multiple output ports are connected to a single input port, the input port will receive each individual signal sent by the outputs.

In the example below, _both_ parameter nodes ("A" and "B") receive the signal to their "read" input, telling them to send out the value they store. Then the "log" node receives and prints out both signals sent by the parameter nodes.

{% hint style="warning" %}
The order of sending signals through one-to-many connections, and the order of receiving signals through many-to-one connections is _not determined_. Eg. in the example below, the order of "A" and "B" appearing th the output window is incidental.
{% endhint %}

![One-to-many and many-to-one](<../../.gitbook/assets/Screenshot 2022-06-25 at 13.39.27.png>)

{% hint style="info" %}
Traffic flowing through connections can be observed by right clicking on the connection and selecting "Show traffic".

![](<../../.gitbook/assets/Screenshot 2022-06-25 at 13.59.27.png>)
{% endhint %}
