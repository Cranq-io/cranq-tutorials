# Dataflow programming

CRANQ, as a programming language, is based on a special flavor of [dataflow programming](https://en.wikipedia.org/wiki/Dataflow\_programming). The details are quite technical, but it can be put in simple terms following the analogy between dataflow programming and _logistics_: after all, dataflow programming is also all about 'handling' and 'distributing' 'materials'. Only in CRANQ, the 'materials' are [signals](signal.md), 'handling' refers to the processing of signals that takes place in [nodes](node.md), and 'distribution' is transmitting signals from one node to another. Unlike physical materials though, signals can be duplicated, destroyed, and created out of thin air. But everything else is the same.

{% hint style="info" %}
An illustration of dataflow programming using an everyday analogy is doing laundry:

1. You take dirty clothes ([signal](signal.md)) to the washing machine ([node](node.md)), where they get clean and wet (signal state changes).
2. Then you put the clean, wet clothes (output from previous node received through a connection) into the dryer (another node), where they become dry and wrinkled (state changes again).
3. Finally, you iron (node) the dry, wrinkled clothes (last output), and end up with unwrinkled ones (final output).
{% endhint %}
