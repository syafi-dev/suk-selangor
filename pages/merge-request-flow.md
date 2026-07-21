---
layout: default
transition: slide-left
clicks: 5
---

<script setup>
const nodes = [
  { shape: 'stadium', cx: 85,  cy: 70, w: 120, h: 48, icon: 'source-branch',        color: 'purple', label: 'Branch',  at: 0 },
  { shape: 'stadium', cx: 265, cy: 70, w: 120, h: 48, icon: 'server',               color: 'blue',   label: 'Push',    at: 1 },
  { shape: 'stadium', cx: 445, cy: 70, w: 130, h: 48, icon: 'file-document-outline', color: 'blue',   label: 'Open MR',  at: 2 },
  { shape: 'stadium', cx: 630, cy: 70, w: 120, h: 48, icon: 'scale-balance',         color: 'amber',  label: 'Review',  at: 3 },
  { shape: 'stadium', cx: 805, cy: 70, w: 120, h: 48, icon: 'check-bold',            color: 'green',  label: 'Merge',   at: 4 },
]
const edges = [
  { at: 1, d: 'M145 70 H200', ax: 205, ay: 70, adeg: 0 },
  { at: 2, d: 'M325 70 H375', ax: 380, ay: 70, adeg: 0 },
  { at: 3, d: 'M510 70 H565', ax: 570, ay: 70, adeg: 0 },
  { at: 4, d: 'M690 70 H740', ax: 745, ay: 70, adeg: 0 },
]
</script>

### The Merge Request: how work ships

<div class="mt-8 max-w-4xl mx-auto">
  <FlowGraph :nodes="nodes" :edges="edges" :width="880" :height="140" />
</div>

<div v-click="5" class="pop grid grid-cols-4 gap-5 mt-10 max-w-4xl mx-auto text-center">
  <div><mdi-comment-check-outline class="text-2xl text-green-600 dark:text-green-400" /><p class="text-sm opacity-75 mt-2 m-0">Review before main</p></div>
  <div><mdi-forum-outline class="text-2xl text-green-600 dark:text-green-400" /><p class="text-sm opacity-75 mt-2 m-0">A discussion trail</p></div>
  <div><mdi-robot-outline class="text-2xl text-green-600 dark:text-green-400" /><p class="text-sm opacity-75 mt-2 m-0">CI/CD runs tests</p></div>
  <div><mdi-history class="text-2xl text-green-600 dark:text-green-400" /><p class="text-sm opacity-75 mt-2 m-0">History stays clean</p></div>
</div>

<!--
- the Merge Request is how a change actually reaches main on a team; you never merge to main privately
[click] you push your feature branch up to GitLab
[click] you open a Merge Request proposing to fold it into main
[click] a teammate reviews the diff, comments, approves
[click] GitLab merges it in, with the whole conversation attached
[click] why bother instead of merging locally: a second pair of eyes before it hits main, a record of why the change was made, automated tests on every push, and a clean documented history
- gloss: an MR is like a pull-request cover note; "here's my change, please check it before it goes live"
-->
