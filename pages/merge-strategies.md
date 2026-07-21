---
layout: default
transition: slide-left
clicks: 2
---

<script setup>
const blue = '#2563eb', purple = '#7c3aed', green = '#16a34a'
// fast-forward: one straight line, the pointer just slides to the tip
const ffCommits = [
  { id: 'A', x: 90,  y: 175, color: blue,  at: 0 },
  { id: 'B', x: 220, y: 175, color: blue,  at: 0 },
  { id: 'C', x: 350, y: 175, color: green, at: 0 },
]
const ffWires = [
  { d: 'M40 175 H90',   color: blue,  at: 0 },
  { d: 'M90 175 H220',  color: blue,  at: 0 },
  { d: 'M220 175 H350', color: green, at: 0 },
]
const ffLabels = [{ text: 'main', x: 40, y: 162, color: blue, at: 0 }]
const ffHead = [[350,175]]
// 3-way: a branch diverges and a merge commit joins both parents
const twCommits = [
  { id: 'A', x: 90,  y: 175, color: blue,   at: 0 },
  { id: 'B', x: 200, y: 175, color: blue,   at: 0 },
  { id: 'f', x: 300, y: 85,  color: purple, at: 0 },
  { id: 'C', x: 330, y: 175, color: blue,   at: 0 },
  { id: 'M', x: 450, y: 175, color: green,  at: 0 },
]
const twWires = [
  { d: 'M40 175 H90',   color: blue, at: 0 },
  { d: 'M90 175 H200',  color: blue, at: 0 },
  { d: 'M200 175 H330', color: blue, at: 0 },
  { d: 'M330 175 H450', color: blue, at: 0 },
  { d: 'M200 175 C 240 175,260 85,300 85', color: purple, at: 0 },
  { d: 'M300 85 C 360 85,400 175,450 175', color: green,  at: 0 },
]
const twLabels = [
  { text: 'main', x: 40, y: 162, color: blue, at: 0 },
  { text: 'feature', x: 250, y: 66, color: purple, at: 0 },
]
const twHead = [[450,175]]
</script>

### Two ways a merge happens

<div class="grid grid-cols-2 gap-10 mt-8 items-center">

<div>
  <p class="text-center text-sm font-700 text-green-600 dark:text-green-400 mb-1">Fast-forward</p>
  <GitGraph :commits="ffCommits" :wires="ffWires" :labels="ffLabels" :head="ffHead" />
  <p class="text-center text-sm opacity-65 mt-1">Main hadn't moved — the pointer just slides forward. No merge commit.</p>
</div>

<div v-click="1">
  <p class="text-center text-sm font-700 text-purple-600 dark:text-purple-400 mb-1">3-way merge</p>
  <GitGraph :commits="twCommits" :wires="twWires" :labels="twLabels" :head="twHead" />
  <p class="text-center text-sm opacity-65 mt-1">Both lines moved — Git makes a new merge commit joining them.</p>
</div>

</div>

<div v-click="2" class="mt-6 text-center text-base opacity-80">
Same command, <code>git merge</code> — Git picks the shape for you.
</div>

<!--
- there are only two shapes a merge can take; you never choose, Git decides from the history
- fast-forward: nobody else changed main while you worked, so Git just moves the main pointer up to your tip; the history stays a straight line
[click] 3-way: both main and your branch moved, so Git cannot just slide the pointer; it creates one new merge commit with two parents to join them
[click] you run the same git merge either way; the shape is automatic
- gloss: fast-forward is like adding pages to the end of a book; a 3-way merge is stapling two chapters back together
-->
