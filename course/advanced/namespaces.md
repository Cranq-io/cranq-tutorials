# Namespaces

Namespaces are ephemeral - they don't exist in themselves, only inasmuch as a node declares them. For instance, the node `data/array/Mapper` belongs to the `data/array` and `data` namespaces, but if someone were to rename it to `data/list/Mapper`, it would belong to `data/list` instead of `data/array` onward, leaving all other nodes in `data/array` unaffected.
