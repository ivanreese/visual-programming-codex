![](/assets/app-store-illustration/hero.webp)

# Impressions: Some random App Store illustration

I saw this illustration as part of [a Featured App story](https://apps.apple.com/ca/story/id1529202557) on the Mac App Store.

The app itself is some sort of flowchart mind-mapping tool by Corel that is, sadly, *far* less interesting than the imaginary VPL in this illustration.

(Also, the app is called "MindManager", which is the most soul-crushing name for an app that I've heard all year. May the ghost of Engelbart haunt anyone who thinks a mind ought to be *managed* by software.)

So, what is it about this illustration that's so interesting? On the one hand, it's just typical node-wire programming viewed through the [Corporate Memphis](https://en.wikipedia.org/wiki/Corporate_Memphis) lens. But on the other hand, there's a bunch of made-up detail that is suggestive of a rich possibility space — much richer than [all those established node-wire languages](https://github.com/ivanreese/visual-programming-codex/blob/main/implementations.md) have actually explored.

<br><br>

## Nodes

The design of each node communicates through color, shape, arrangement, texture, silhouette, rhythm, and more. These are nodes designed by someone who spent many years of their life deeply studying and honing the craft of graphic design / visual communication. The drawing is meant to be eye-catching, sure, but the person who made it is a proper *designer*, so they didn't just draw "whatever" — there are consistent, systemic details here. I don't imagine the illustrator actually thought too much about how things would *work*, but I'd be quite surprised if they didn't think about what things *meant*.

Compare this with so-called "visual programming languages" where the nodes all look the same except for the text you put in them. Come on!

<br><br><br>

![](/assets/app-store-illustration/matrix.webp)

This node looks like some sort of matrix, with a grid where various cells are filled with dots. The dots are differently coloured, suggesting that these cells could be enums or even composite values.

Could be similar to the [matrixctrl](https://docs.cycling74.com/max8/refpages/matrixctrl) in Max/MSP:

![](/assets/app-store-illustration/matrixctrl.png)

<br><br><br>

![](/assets/app-store-illustration/spreadsheet.webp)

Hell, you could put a little spreadsheet on your node. Has anyone ever put a nice little spreadsheet-like interface onto the surface of a node? Why the hell not?

<br><br><br>

![](/assets/app-store-illustration/pie.webp)

These nodes have little pie charts hanging off of them. Cute! Some sort of progress indicator for a long running task? An indication of how much each node contributes to the perf cost of executing the entire graph? An exp tracker showing how close you are to levelling-up the node and unlocking its next feature?

<br><br><br>

![](/assets/app-store-illustration/standards.webp)

Even though each node seems specialized for a particular function, there's a common theme across all the nodes. They have some sort of shape on the left side of the node — either a circle or a roundrect, with a dot in the center. Both the size and color of the dot and the shape vary. So no matter what the function of each individual node is, they all have this element in common. Maybe this is where you click and drag to create a new wire?

The one exception to the above pattern is this node in the center:

![](/assets/app-store-illustration/exception.webp)

This node has a unique shape, unique contents, and a fairly unique style of wire leading into it. It could be that this node is just an informational display rather than a function or computational object.

<br><br>

## Wires

Wires are much more robust than you typically see. They're thick, and colorful. You could almost imagine little abstract representations of your data flowing through these pipes like water.

![](/assets/app-store-illustration/wires.webp)

I'm a strong believer that wires are the most underdeveloped part of visual programming tools.

* In most VPLs, when you disconnect a wire from a node and then let go of the wire, the wire is immediately deleted. So there's only 2 valid states for a wire — either connected to a node on both ends, or connected to a node on one end and the mouse cursor on the other end. I think this is a mistake. I think the wire should continue to exist until you explicitly delete it. If you want to draw a wire freely in space, not connected to any nodes, good! If you want to unplug a wire from a node, and then put the wire down for a moment while you go get a different node ready, good! You should be able to think of wires the way you think of physical cables in the real world, except that they can be whatever length you want, never get tangled, and can show you what's going on inside them.
* Wires tend to be straight lines, S-curves, or some other shape that is completely outside the control of the programmer. I think this is a mistake. Rare is the VPL that lets you choose what path the wire should take. Rarer still is the VPL that lets you work with wires using a robust set of tools — braiding multiple wires together, choosing the color or texture of wires, offering different kinds of wires that are specialized for specific tasks, drawing elegantly curving wires with an inkpen tool, manipulating individual vertices or bezier curves, adding "hints" to help an autolayout system route your wires intelligently.

I also think the wires in this illustration are much weaker than the nodes. They don't show any indication of affordances for interaction. There's no hint of live data being conveyed through them. They don't have a sense of material. But they're still better than what all the other VPLs are doing, so let's dig in.

<br><br><br>

![](/assets/app-store-illustration/fork.webp)

Here's a wire that forks! That's nice and clean-looking, and the meaning is clear. Engineers are comfortable working with bus networks, and electrical engineers are quite used to the idea that "electricity is gonna go everywhere it can", so we could easily come up with programming semantics that allow data to behave similarly. Start with graphic design, and work backward toward semantics, and you'll find some really compelling possibilities.

<br><br><br>

![](/assets/app-store-illustration/arrows.webp)

Some wires have arrows. Arrows clearly telegraph both the direction of flow, and *the fact that flow is directional*. This would be handy in a VPL that allowed computation to be bidirectional by default, but offered unidirectional flow as an option, or as a fallback when a bidirectional relationship isn't possible. The display of arrows could be handled automatically by the environment and/or manually by the programmer. You might not need to see the arrows if the direction of flow is unambiguous for you most of the time, but you might put arrows on the wires where your node arrangement makes flow direction a little hard to intuit. Arrows could also be animated to travel along the wires, showing the fact that flow is occurring, the direction of flow, and the rate of flow (animation speed), the density of flow (arrow spacing), and other information (arrow size, arrow color, arrow shape).

This is low-hanging fruit, y'all!

<br><br><br>

![](/assets/app-store-illustration/wires.webp)

The wires can be different thicknesses, and can have color and texture that changes along the length of the wire. These are opportunities to communicate subtle hints about the runtime state of the program, without adding much in the way of visual noise (as opposed to, say, a text HUD) or context switching (like some debug view separate from the source program).

<br><br><br>

![](/assets/app-store-illustration/annotations.webp)

In this illustration, wires have little annotations on them.

Hey, a comment bubble! It's almost as though this imaginary visual programming environment was designed to be used by multiple people who want to communicate the specific intent behind the structure of the code. *What a novel idea.*

The (+) icon is the one thing that, to me, feels like it was thrown in just for the hell of it, without much utility. Or maybe this is data being conveyed along the wires, depicted abstractly. In any case, the idea that your wires can have stuff on/in them is a powerful idea, even if this made-up example doesn't actually flesh-out the idea.

<br><br>

## General

<br>

![](/assets/app-store-illustration/hero.webp)

Nodes are arranged in 3d space around the programmer. The programmer is able to grab one of the nodes out of the air with their fingers. The interface elements seem suitable for physical interaction.

When we have the [Holodeck](https://en.wikipedia.org/wiki/Holodeck)-ass technology to do this, I don't want to see *anyone* using a text-based language in a terminal.
