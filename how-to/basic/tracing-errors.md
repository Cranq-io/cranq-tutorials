# Tracing errors

Sometimes, when errors happen, nodes turn red in activity view instead of green. Errors may occur anywhere in the code, at any depth of the graph, but CRANQ 'bubbles' the errors (and also warnings) up along the chain of parent nodes, so when you spot a red node, all you have to do to find the node that threw it is drill down along red nodes until you find a red code node.

Errors are always thrown by code nodes, and they are usually caused by two problems:

* There may be a bug in the JavaScript that implements the code node, but this is rare. Buggy JavaScript in code nodes has to be fixed at that level.
* What's actually much more likely, is that a port received data that it didn't expect. In this case, you need to look at the received signal and node that sent it.
