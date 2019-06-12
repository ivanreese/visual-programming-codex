![](assets/cinema-4d-xpresso.png)

## Impressions: [Cinema 4D Xpresso](implementations.md#cinema-4d-xpresso)

Like:

* Input and output port order can be drag-adjusted to cut down on crossed wires.

* Groups — They behave like subpatchers in that they're a cropped view into their contents, that can be panned/zoomed/collapsed from the outside, and they can be saved/loaded for reuse across projects. Execution of the grouped nodes can be toggled on and off, and this can be controlled by outside nodes.

Dislike:

* Almost zero liveness within the patcher interface, save for debug nodes that display the most recent value passed to them. The surrounding Cinema 4D environment live updates in response to Xpresso, and you can create sliders and other UI widgets in the attributes panel and use as IO for nodes.

* Only one UI paradigm — no facility for custom creation of nodes, nodes as custom I/O, etc. Squint and all nodes look the same. This extends to math where each term in an expression is a node, including constants, and nodes like Add don't appear to be variadic, alas.

* Wires appear to be limited to simple S-curves, with no advanced routing.

* "If the connection is not allowed, the wire will be deleted as soon as you release the mouse button."

* No feedback loops, period.
