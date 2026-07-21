---
layout: default
transition: slide-left
---

### Two classics you'll actually hit

<div class="grid grid-cols-2 gap-8 mt-5 items-start">

<div v-click="1">
  <p class="font-700 flex items-center gap-2 mb-2"><mdi-emoticon-dead-outline class="text-amber-600 dark:text-amber-400" /> Committed to main by mistake</p>
  <div class="term-print">
  <TermWindow title="move it to a branch">
    <div class="opacity-50"># still on main, commit made</div>
    <div><span class="text-green-400">$</span> git switch -c feature/rescue</div>
    <div><span class="text-green-400">$</span> git switch main</div>
    <div><span class="text-green-400">$</span> git reset --hard origin/main</div>
  </TermWindow>
  </div>
  <p class="text-sm opacity-65 mt-2">Your commit is safe on <code>feature/rescue</code>; main matches the remote again.</p>
</div>

<div v-click="2">
  <p class="font-700 flex items-center gap-2 mb-2"><mdi-magnify class="text-amber-600 dark:text-amber-400" /> "I lost a commit!"</p>
  <div class="term-print">
  <TermWindow title="reflog remembers">
    <div><span class="text-green-400">$</span> git reflog</div>
    <div class="opacity-50"># find the lost commit's hash</div>
    <div><span class="text-green-400">$</span> git switch -c rescue &lt;hash&gt;</div>
  </TermWindow>
  </div>
  <p class="text-sm opacity-65 mt-2">After a bad reset or deleted branch, Git rarely throws anything away.</p>
</div>

</div>

<div v-click="3" class="mt-6 flex items-center justify-center gap-2 caution text-base">
  <mdi-hand-back-right class="flex-shrink-0" /> Golden rule: when unsure, STOP and ask. Don't pile commands on a mess.
</div>

<!--
[click] committed to main when you meant to be on a branch: make a branch here (it keeps the commit), switch back to main, and reset --hard to origin/main so main matches the server again; your work is safe on the rescue branch
[click] "I lost a commit" after a bad reset or a deleted branch: reflog is Git's memory of everywhere HEAD has been; find the hash and make a branch from it; the commit is back
[click] the golden rule: the fastest way to make a mess worse is to keep typing; when unsure, stop and ask
- reassure: reset --hard sounds scary but here it only moves main to match the remote, and the commit already lives on the rescue branch
-->
