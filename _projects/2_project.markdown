---
layout: page
title: my swift playground stage
description: try to solve this!
img: /assets/img/3.jpg
importance: 2
category: work
---

Every project has a beautiful feature showcase page.
It's easy to include images in a flexible 3-column grid format.
Make your photos 1/3, 2/3, or full width.

To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---

<pre><code>
let target = Character()
world.place(Gem(), atColumn: 0, row: 5)
world.place(Switch(), atColumn: 7, row: 6)
for i in 1 ... 6 {
    world.place(Block(), atColumn: i, row: 3)
}
for i in 1 ... 6 {
    world.place(Block(), atColumn: i, row: 3)
}
let greenPortal = Portal(color:  colorLiteral(red: -0.24377164244651794, green: 0.7537863850593567, blue: -0.22403845191001892, alpha: 1.0))
world.place(greenPortal, atStartColumn: 0, startRow: 3, atEndColumn: 2, endRow:7)
let redPortal = Portal(color:  colorLiteral(red: 1.0929099321365356, green: -0.22076299786567688, blue: -0.09911013394594193, alpha: 1.0))
world.place(redPortal, atStartColumn: 2, startRow: 1, atEndColumn: 5, endRow:5)
let bluePortal = Portal(color:  colorLiteral(red: 0.0028873691335320473, green: 0.37862303853034973, blue: 0.992986261844635, alpha: 1.0))
world.place(bluePortal, atStartColumn: 6, startRow: 1, atEndColumn: 2, endRow: 4)
world.place(Platform(), atColumn: 3, row: 4)
world.place(Block(), atColumn:4, row:1)
world.place(Block(), atColumn:4, row:2)
world.place(Platform(), atColumn: 4, row: 1)
world.place(target, atColumn: 3, row: 2)
</code></pre>


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/stage.png' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    My stage. Can you try to solve it?
</div>

