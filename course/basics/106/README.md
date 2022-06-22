---
description: >-
  Walks you through practices for identifying and eliminating problems in the
  code.
---

# 105: Debugging

Where the visual nature of CRANQ really shines, is monitoring and debugging running programs.

CRANQ code is a graph - so it seems natural for all kinds of data to be overlaid on top of it. The first, and perhaps most useful overlay shows what happens in the graph while the program is running. As soon as you click "Run" or hit Cmd / Ctrl + R, the app switches into "Activity" view, and the entire graph turns grey. Grey indicates inactivity in nodes and connections. As the program starts however, nodes that got activated turn green. As the program continues to run, you can _see_ nodes activating in realtime.

Moreover, the data flowing through connections can also be observed by opening a "Traffic viewer" window from the connection's context menu, displaying the last signal transmitted over that particular connection (data and tag). By having a few of these traffic viewers open you can monitor the transformation of data through the nodes in view.

{% hint style="info" %}
[Currently](../../../roadmap.md#types-traffic-viewers), traffic viewers can only display data as JSON.
{% endhint %}

## Tracing errors

Sometimes, when errors happen, nodes turn red in activity view instead of green. Errors may occur anywhere in the code, at any depth of the graph, but CRANQ 'bubbles' the errors (and also warnings) up along the chain of parent nodes, so when you spot a red node, all you have to do to find the node that threw it is drill down along red nodes until you find a red code node.

Errors are always thrown by code nodes, and they are usually caused by two problems:

* There may be a bug in the JavaScript that implements the code node, but this is rare. Buggy JavaScript in code nodes has to be fixed at that level.
* What's actually much more likely, is that a port received data that it didn't expect. In this case, you need to look at the received signal and node that sent it.

## Stuck signals

Most bugs in CRANQ don't surface as errors. They are caused by nodes not sending the expected output in response to the input they receive. In other words, the most common symptom of buggy CRANQ code is signals being stuck.

Stuck signals are just as easy to localize as errors, but we're looking for different visual cues. Instead of red nodes, they're indicated by nodes that received input (green upstream connections), but did not send all of the expected output (some or all downstream connections are grey).
