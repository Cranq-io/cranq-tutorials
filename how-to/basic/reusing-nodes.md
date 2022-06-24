# Reusing nodes

As important as good grouping is, documenting nodes is perhaps even more important, if you want your new node to be used by others. Well documented nodes are much easier to find in the repo.

If you want to make a node reusable, first you need to flip the corresponding switch on the node's prototype panel. From this point on, the node is discoverable in the repo as a _prototype_.

* Give the prototype a name that describes what it does as concisely as possible.
* Place it in a namespace that makes sense. It's a good idea to check whether namespace you have in mind exists, and if it does, what's in it.
* Write a description for the node, expanding on what it does in a bit more detail than the name. Add examples and links to the description if possible.
* Assign an icon to the prototype that reflects its purpose, or makes an external service or API recognizable.
* Clean up ports and (re)name them meaningfully. During grouping, sometimes you get duplicated ports from multiple connections going to the same port in the parent.
* Assign data types to the ports. For the time being these data types are just for documentation, but we're working hard towards types being a basis for determining connections' validity, as well as properties to search nodes by. Data types will become very important in the near future.

If you do the above, your brand new reusable node will be easy to find and easy to work with.
