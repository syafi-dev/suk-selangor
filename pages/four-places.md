---
layout: default
transition: slide-left
clicks: 4
---

<script setup>
const nodes = [
  { shape: 'rect', cx: 95,  cy: 100, w: 150, h: 54, icon: 'folder-outline', color: 'slate',  label: 'Working dir', at: 0 },
  { shape: 'rect', cx: 330, cy: 100, w: 150, h: 54, icon: 'file-multiple', color: 'amber',  label: 'Staging area', at: 1 },
  { shape: 'rect', cx: 565, cy: 100, w: 150, h: 54, icon: 'source-branch', color: 'cyan',   label: 'Local repo', at: 2 },
  { shape: 'rect', cx: 800, cy: 100, w: 150, h: 54, icon: 'server',        color: 'blue',   label: 'Remote (GitLab)', at: 3 },
]
const edges = [
  { at: 1, d: 'M175 100 H250', ax: 250, ay: 100, adeg: 0, lx: 212, ly: 80, lw: 62,  label: 'git add',    lc: 'amber' },
  { at: 2, d: 'M410 100 H485', ax: 485, ay: 100, adeg: 0, lx: 447, ly: 80, lw: 84,  label: 'git commit', lc: 'cyan' },
  { at: 3, d: 'M645 100 H720', ax: 720, ay: 100, adeg: 0, lx: 682, ly: 80, lw: 70,  label: 'git push',   lc: 'blue' },
]
</script>

### Four places your code lives

<div class="mt-10 max-w-4xl mx-auto">
  <FlowGraph :nodes="nodes" :edges="edges" :width="880" :height="170" />
</div>

<div v-click="4" class="mark-safe mt-8 text-center text-lg opacity-85">
<code>git status</code> is your map — it names <span v-mark="{ at: 4, color: '#dc2626', type: 'underline' }">which zone</span> each change sits in.
</div>

<!--
- the number-one source of confusion: the same file can be in a different state in each of four places
[click] you edit in the working directory, the files you see right now; git add moves a change into staging
[click] staging is the "ready to save" basket, you choose exactly what goes in; git commit saves it
[click] commit writes it into your local repository, the history on your own machine; git push shares it
[click] push sends it to the remote on GitLab, the shared source of truth for the team
- so run git status constantly; it tells you which of the four zones every change is in right now
- gloss: staging is like putting items on the checkout belt before you pay; commit is the receipt
-->
