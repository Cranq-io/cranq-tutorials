# Grouping

The process of grouping is fairly straightforward: select the nodes you want to group (Cmd / Ctrl + click), open the context menu on one of the selected nodes (right click), then pick "Group nodes". That's it.

However, the way you group makes all the difference, as this is what imposes structure on code. _Well structured CRANQ code is easy to understand and navigate._

Grouping well is not hard at all. If you stick to these best practices, you'll be acing CRANQ:

* Nodes should ideally contain no more than 7 children.\
  This helps keeping the mental load as low as possible_._ No one wants to look at a graph that's tangled beyond understanding.
* Group nodes that together achieve something that you can name. \
  Being able to name a collection of nodes is a good indication that the grouping is justified. If you can't give it a name, try grouping differently.
* Give children names that make out sequences of changes when read along connections. Understanding a graph is easier when you can tell what's happening by just following the connections.
