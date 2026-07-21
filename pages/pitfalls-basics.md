---
layout: default
transition: slide-up
---

<p class="eyebrow font-mono"><span class="text-red-600 dark:text-red-400">part 1</span> &middot; git core refresher</p>

### Common mistakes in the basics

<div class="pop grid grid-cols-2 gap-x-14 gap-y-8 mt-8 max-w-4xl mx-auto">

<div v-click="1" class="flex items-start gap-3">
  <mdi-close-circle class="text-2xl pf-cross flex-shrink-0 mt-0.5" />
  <div>
    <p class="font-700 m-0">Committing everything with <code>git add .</code></p>
    <p class="text-sm opacity-65 mt-1 mb-1">You sweep up junk, secrets, or half-done files.</p>
    <p class="text-sm pf-check m-0"><mdi-check class="inline" /> Add only what you mean to</p>
  </div>
</div>

<div v-click="2" class="flex items-start gap-3">
  <mdi-close-circle class="text-2xl pf-cross flex-shrink-0 mt-0.5" />
  <div>
    <p class="font-700 m-0">Vague commit messages</p>
    <p class="text-sm opacity-65 mt-1 mb-1">"update", "fix", "asdf" — useless in six months.</p>
    <p class="text-sm pf-check m-0"><mdi-check class="inline" /> One clear line: what &amp; why</p>
  </div>
</div>

<div v-click="3" class="flex items-start gap-3">
  <mdi-close-circle class="text-2xl pf-cross flex-shrink-0 mt-0.5" />
  <div>
    <p class="font-700 m-0">Forgetting to pull first</p>
    <p class="text-sm opacity-65 mt-1 mb-1">You start from stale code and make needless conflicts.</p>
    <p class="text-sm pf-check m-0"><mdi-check class="inline" /> Pull, then work</p>
  </div>
</div>

<div v-click="4" class="flex items-start gap-3">
  <mdi-close-circle class="text-2xl pf-cross flex-shrink-0 mt-0.5" />
  <div>
    <p class="font-700 m-0">Committing secrets &amp; big files</p>
    <p class="text-sm opacity-65 mt-1 mb-1">Passwords, <code>.env</code>, <code>node_modules</code> live in history forever.</p>
    <p class="text-sm pf-check m-0"><mdi-check class="inline" /> Use <code>.gitignore</code> from the start</p>
  </div>
</div>

</div>

<!--
- four mistakes people make in the basics; each has a one-line habit that prevents it
[click] git add . sweeps up everything, including things you did not mean to share; stage deliberately or check status first
[click] a vague message is useless later; write what changed and why, like "Fix login redirect on timeout"
[click] not pulling first means you build on old code and create conflicts you did not need; pull before each session
[click] secrets and huge folders end up in history permanently; a .gitignore from day one keeps them out
- we practise the .gitignore fix properly in Part 3
-->
