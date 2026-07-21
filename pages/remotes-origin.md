---
layout: default
transition: slide-left
clicks: 3
---

<script setup>
const nodes = [
  { shape: 'rect', cx: 180, cy: 100, w: 220, h: 72, icon: 'laptop', color: 'cyan', label: 'Local repository', at: 0 },
  { shape: 'rect', cx: 640, cy: 100, w: 220, h: 72, icon: 'server', color: 'blue', label: 'Remote (origin)', at: 0 },
]
const edges = [
  { at: 1, d: 'M296 82 H514',  ax: 520, ay: 82,  adeg: 0,   lx: 408, ly: 68,  lw: 66, label: 'git push', lc: 'cyan' },
  { at: 2, d: 'M514 120 H302', ax: 296, ay: 120, adeg: 180, lx: 408, ly: 134, lw: 78, label: 'git pull',  lc: 'blue' },
]
</script>

### Remotes & "origin"

<p class="text-sm opacity-60 mt-1 mb-2">A remote is your project hosted on GitLab. <code>origin</code> is the default nickname for the one you cloned from.</p>

<div class="mt-6 max-w-4xl mx-auto">
  <FlowGraph :nodes="nodes" :edges="edges" :width="820" :height="200" />
</div>

<div v-click="3" class="mt-2 text-center text-sm opacity-75">
See your remotes: <code>git remote -v</code> &nbsp;·&nbsp; push a brand-new branch: <code>git push -u origin &lt;branch&gt;</code>
</div>

<!--
- a remote is just your project living somewhere else, on GitLab; you commit locally, then sync with it
[click] git push sends your local commits up to the remote so the team sees them
[click] git pull brings the team's commits down to you; the two directions keep you in sync
[click] origin is only a nickname for the remote you cloned from; remote -v lists them; the -u flag on the first push links your new branch to origin so later you can just type git push
- gloss: origin is a saved contact name for the server address, so you never retype the full URL
-->
