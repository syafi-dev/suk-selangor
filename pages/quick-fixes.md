---
layout: default
transition: slide-left
---

### If this happens… do this

<div class="mt-6 max-w-4xl mx-auto">

<div class="grid grid-cols-[1fr_1.1fr] gap-x-8 pb-2 mb-2 border-b border-gray-400/25 text-xs font-mono tracking-widest uppercase opacity-50">
  <div>Symptom</div><div>Fix</div>
</div>

<div class="space-y-3">
  <div v-click="1" class="grid grid-cols-[1fr_1.1fr] gap-x-8 items-center"><div>Push rejected (non-fast-forward)</div><div class="font-mono text-sm text-amber-600 dark:text-amber-400">git pull → resolve → git push</div></div>
  <div v-click="2" class="grid grid-cols-[1fr_1.1fr] gap-x-8 items-center"><div>Committed to the wrong branch</div><div class="font-mono text-sm text-amber-600 dark:text-amber-400">branch off it, reset the wrong one back</div></div>
  <div v-click="3" class="grid grid-cols-[1fr_1.1fr] gap-x-8 items-center"><div>Typo in last commit message</div><div class="font-mono text-sm text-amber-600 dark:text-amber-400">git commit --amend  (before pushing)</div></div>
  <div v-click="4" class="grid grid-cols-[1fr_1.1fr] gap-x-8 items-center"><div>Staged a file by accident</div><div class="font-mono text-sm text-amber-600 dark:text-amber-400">git restore --staged &lt;file&gt;</div></div>
  <div v-click="5" class="grid grid-cols-[1fr_1.1fr] gap-x-8 items-center"><div>Need to undo a pushed change</div><div class="font-mono text-sm text-amber-600 dark:text-amber-400">git revert &lt;hash&gt;  (team-safe)</div></div>
  <div v-click="6" class="grid grid-cols-[1fr_1.1fr] gap-x-8 items-center"><div>Merge going wrong</div><div class="font-mono text-sm text-amber-600 dark:text-amber-400">git merge --abort  and start over</div></div>
</div>

</div>

<!--
- this is the "keep it open on your second monitor" table; symptom on the left, the fix on the right
[click] rejected push means someone pushed first: pull, resolve any conflict, push again
[click] wrong branch: branch off to save the commit, then reset the wrong branch back
[click] message typo: amend, but only before you have pushed
[click] accidental stage: restore --staged pulls it back out
[click] undo something already pushed: revert, which is safe for the team
[click] a merge going sideways: merge --abort rewinds you and you start clean
- these are all things we practised; this slide is just the index to them
-->
