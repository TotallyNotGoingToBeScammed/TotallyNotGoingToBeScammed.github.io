---
layout: page
title: Swift Playground Code
description: some swift playground stages I made
img: /assets/img/12.jpg
importance: 1
category: work
---

This is a solve to r/swiftplayground's top puzzle, written in swift.

It took me a while to realize the one if loop and two turnRight() are good enough though... Anyone has any simpler solutions?

<pre><code>if (!isBlockedLeft) {
turnLeft()
} else if (!isBlocked) {
// NULL - going to move forward
} else if (!isBlockedRight) {
turnRight()
} else {
// Turning around
turnRight()
turnRight()
}
moveForward()</code></pre>
