---
layout: default
transition: slide-left
---

### Everyday branching commands

<div class="grid grid-cols-2 gap-8 items-center mt-4">

<div class="term-print">
<TermWindow title="branching">
<div v-click="1" class="opacity-50"># create AND switch in one step</div>
<div v-click="1"><span class="text-green-400">$</span> git switch -c feature/login</div>
<div v-click="2" class="opacity-50"># ...work, add, commit as usual...</div>
<div v-click="3" class="opacity-50"># go back to main and update it</div>
<div v-click="3"><span class="text-green-400">$</span> git switch main</div>
<div v-click="3"><span class="text-green-400">$</span> git pull</div>
<div v-click="4" class="opacity-50"># fold your feature in</div>
<div v-click="4"><span class="text-green-400">$</span> git merge feature/login</div>
</TermWindow>
</div>

<div class="space-y-5">
  <div v-click="1" class="note-row items-center"><mdi-swap-horizontal class="note-ico text-purple-600 dark:text-purple-400" /><p><b>git switch</b> <span class="opacity-60">· change branches (checkout still works)</span></p></div>
  <div v-click="2" class="note-row items-center"><mdi-plus-circle-outline class="note-ico text-purple-600 dark:text-purple-400" /><p><b>git switch -c</b> <span class="opacity-60">· create a branch and jump on</span></p></div>
  <div v-click="3" class="note-row items-center"><mdi-format-list-bulleted class="note-ico text-purple-600 dark:text-purple-400" /><p><b>git branch</b> <span class="opacity-60">· list them; -d deletes a merged one</span></p></div>
  <div v-click="4" class="note-row items-center"><mdi-tag-outline class="note-ico text-purple-600 dark:text-purple-400" /><p><b>Naming</b> <span class="opacity-60">· feature/… bugfix/… hotfix/…</span></p></div>
</div>

</div>

<!--
[click] switch -c creates the branch and moves you onto it in one step; the modern replacement for checkout -b
[click] then you work normally: edit, add, commit, all on your branch
[click] when done, switch back to main and pull so main is current before you merge
[click] merge folds your branch into main; name branches for their job so the list reads clearly
- gloss: switch is just "which desk am I sitting at"; the files change to match that branch
-->
