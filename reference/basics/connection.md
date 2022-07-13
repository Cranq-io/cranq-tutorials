# Connection

A connection _transmits_ [signals](broken-reference) from an output port to the connected input port. It also _propagates_ the [parameter](broken-reference) set on a parent node's input port to input ports of connected child nodes.

* When transmitting, connected output ports receive the signals immediately as they appear on the sender's output port.
* When propagating parameters, inherted parameter values get set on connected input ports as you enter them.

## One-to-many and many-to-one

When a single output port has multiple inputs connected, all connected input ports will receive the same signal that was sent by the output.

Similarly, when multiple output ports are connected to a single input port, the input port will receive each individual signal sent by the outputs.

In the example below, _both_ parameter nodes ("A" and "B") receive the signal to their "read" input, telling them to send out the value they store. Then the "log" node receives and prints out both signals sent by the parameter nodes.

{% hint style="warning" %}
The order of sending signals through one-to-many connections, and the order of receiving signals through many-to-one connections is _not determined_. Eg. in the example below, the order of "A" and "B" appearing th the output window is incidental.
{% endhint %}

![One-to-many and many-to-one](<../../.gitbook/assets/Screenshot 2022-06-25 at 13.39.27.png>)

{% hint style="info" %}
Traffic flowing through connections [can be observed](broken-reference) by right clicking on the connection and selecting "Show traffic".

![](<../../.gitbook/assets/Screenshot 2022-06-25 at 13.59.27.png>)
{% endhint %}
