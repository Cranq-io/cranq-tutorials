# Dataflow programming

CRANQ, as a programming language, is based on a special flavor of [dataflow programming](https://en.wikipedia.org/wiki/Dataflow\_programming).

{% hint style="info" %}
The simplest illustration of dataflow programming is doing laundry:

1. You take dirty clothes (signal) to the washing machine (node), where they get clean and wet (state changes).
2. Then you put the clean, wet clothes (output from previous node) into the dryer (another node), where they become dry and wrinkled (state changes again).
3. Finally, you iron (node) the dry, wrinkled clothes (last output), and end up with unwrinkled ones (final output).
{% endhint %}
