### [Deutsch limit](https://en.wikipedia.org/wiki/Deutsch_limit)
> The problem with visual programming is that you can’t have more than 50 visual primitives on the screen at the same time.

* Coined by [Fred Lakin](reflections.md#fred-lakin)

### Abstraction
* It is argued that there aren't many well-explored patterns for abstraction, aside from simply collapsing sections of visual code (akin to subroutines at worst or named functions at best).

### Mousing is Slow
* Typing text subjectively feels faster, perhaps since it's composed of smaller atomic actions.

### Spaghetti
* Crossing lines in node-and-wire languages looks messy, feels messy.

### Scaling
* The most common complaint from people _who have actually tried visual programming_ is that it works well in the small, but becomes untenable past a certain complexity threshold.

### Version control
* There is almost no generic version control systems with visual displaying of diffs (There is workaround with using git for XML generated from document, but this breaks almost all idea for visual programming ("make you free from writing a code"). But there are some implementations https://github.blog/2013-09-17-3d-file-diffs/ )
* Node movement is diff. Parametric connection movement is diff. So each time you made multiple changes which are not changing behaviour (but only visual appearance) will cause hard to read diffs in XML representation.
* Almost impossible to work in team on one document and keep history of changes, especially if editor is not online (but online editor introduces other challenges).
  * How can I made merge request review? There is no visual diff usually, almost all visual programming systems can't display 2 documents on same screen (no capability, and they will not fit 2 big documents on average user display)
  * How can I cherry pick only some changes? Only use git and back to text
  * If there is isolated workspaces for each worker (e.g. blender local document, vivado block diagramm)
    * How can I resolve merge conflicts? Only use git and back to text and enable my imagination how this text will look in UI
  * If there is common workspace for each worker (e.g. google docs)
    * 2 people are working simultaneously on some document. One of them decided revert all current changes he/she made since some checkpoint. This actoin is eigher impossible or really hard to do.
  * How can I see history of changes with comments? Git solves that. There are some history of changes displayed (e.g. google docs), but without comments.
* Conclusion: Using git for visual programming almost breaks UI workflow of most current visual programming tools. You will need switch to text view for almost all common tasks which git makes easy with regular programming launguages
  * e.g. imagine XML and diffs for this https://forum.digilentinc.com/uploads/monthly_2017_03/58cb2b05db14c_wholeblockdiagram.PNG.faed870ae0e68a0adaacee535050906c.PNG 
    * source https://forum.digilentinc.com/topic/3700-vivado-block-diagram-pmodoledrgb_axi_quad_spi_0_0/

### Brooks
In his famous paper [No Silver Bullet](http://worrydream.com/refs/Brooks-NoSilverBullet.pdf), Fred Brooks has a section stating that software suffers from **Invisibility**:

> Invisibility. Software is invisible and unvisualizable. Geometric abstractions are powerful tools. The floor plan of a building helps both architect and client evaluate spaces, traffic flows, views. Contradictions and omissions become obvious. Scale drawings of mechanical parts and stick-figure models of molecules, although abstractions, serve the same purpose. A geometric reality is captured in a geometric abstraction.
> The reality of software is not inherently embedded in space. Hence, it has no ready geometric representation in the way that land has maps, silicon chips have diagrams, computers have connectivity schematics. As soon as we attempt to diagram software structure, we find it to constitute not one, but several, general directed graphs superimposed one upon another. The several graphs may represent the flow of control, the flow of data, patterns of dependency, time sequence, name-space relationships. These graphs are usually not even planar, much less hierarchical. Indeed, one of the ways of establishing conceptual control over such structure is to enforce link cutting until one or more of the graphs becomes hierarchical. [1]
> [1] D.L. Parnas, "Designing Software for Ease of Extension and Contraction," IEEE Transactions on Software Engineering, Vol. 5, No. 2, March 1979, pp. 128-38.

Followed later by a section critiquing **Graphical Programming**:

> A favorite subject for PhD dissertations in software engineering is graphical, or visual, programming — the application of computer graphics to software design. [2] Sometimes the promise held out by such an approach is postulated by analogy with VLSI chip design, in which computer graphics plays so fruitful a role. Sometimes the theorist justifies the approach by considering flowcharts as the ideal program-design medium and by providing powerful facilities for constructing them.
> Nothing even convincing, much less exciting, has yet emerged from such efforts. I am persuaded that nothing will.
> In the first place, as I have argued elsewhere [3], the flowchart is a very poor abstraction of software structure. Indeed, it is best viewed as Burks, von Neumann, and Goldstine's attempt to provide a desperately needed high-level control language for their proposed computer. In the pitiful, multipage, connection-boxed form to which the flowchart has today been elaborated, it has proved to be useless as a design tool — programmers draw flowcharts after, not before, writing the programs they describe.
> Second, the screens of today are too small, in pixels, to show both the scope and the resolution of any seriously detailed software diagram. The so-called "desktop metaphor" of today's workstation is instead an "airplane-seat" metaphor. Anyone who has shuffled a lap full of papers while seated between two portly passengers will recognize the difference — one can see only a very few things at once. The true desktop provides overview of, and random access to, a score of pages. Moreover, when fits of creativity run strong, more than one programmer or writer has been known to abandon the desktop for the more spacious floor. The hardware technology will have to advance quite substantially before the scope of our scopes is sufficient for the software-design task.
> More fundamentally, as I have argued above, software is very difficult to visualize. Whether one diagrams control flow, variable-scope nesting, variable cross references, dataflow, hierarchical data structures, or whatever, one feels only one dimension of the intricately interlocked software elephant. If one superimposes all the diagrams generated by the many relevant views, it is difficult to extract any global overview. The VLSI analogy is fundamentally misleading — a chip design is a layered two-dimensional description whose geometry reflects its realization in 3-space. A software system is not.

> [2] G. Raeder, "A Survey of Current Graphical Programming Techniques," Computer (special issue on visual programming), R.B. Graphton and T. Ichikawa, guest eds., Vol. 18, No. 8, August 1985, pp. 11-25.
> [3] F.P. Brooks, The Mythical Man Month, Reading, Mass.: Addison-Wesley, 1975, Chapter 14.
