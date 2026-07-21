---
layout: default
transition: slide-left
---

### One day, four blocks

<div class="mt-3 mb-5 text-sm opacity-60 flex items-center gap-2">
  <mdi-weather-sunny class="text-amber-500" /> 09:00 warm-up &amp; setup check
  <span class="opacity-30 mx-1">•</span>
  16:45 cheat sheet, Q&amp;A &amp; wrap-up
  <mdi-weather-night class="text-blue-400" />
</div>

<div class="pop grid grid-cols-4 gap-5 mt-4">

<div v-click="1">
  <div class="text-xs font-mono text-red-600 dark:text-red-400 font-700">09:30</div>
  <div class="medallion !w-12 !h-12 !mx-0 my-3 bg-red-500/10"><mdi-sync class="text-2xl text-red-600 dark:text-red-400" /></div>
  <p class="font-700 m-0">Part 1 · Git Core</p>
  <p class="text-sm opacity-65 mt-1 mb-0">The daily cycle · Labs 1–2 · basic pitfalls</p>
</div>

<div v-click="2">
  <div class="text-xs font-mono text-purple-600 dark:text-purple-400 font-700">11:00</div>
  <div class="medallion !w-12 !h-12 !mx-0 my-3 bg-purple-500/10"><mdi-source-branch class="text-2xl text-purple-600 dark:text-purple-400" /></div>
  <p class="font-700 m-0">Part 2 · Branching</p>
  <p class="text-sm opacity-65 mt-1 mb-0">Branch flow · Labs 3–5 · merge conflicts</p>
</div>

<div v-click="3">
  <div class="text-xs font-mono text-blue-600 dark:text-blue-400 font-700">14:00</div>
  <div class="medallion !w-12 !h-12 !mx-0 my-3 bg-blue-500/10"><logos-gitlab-icon class="text-2xl" /></div>
  <p class="font-700 m-0">Part 3 · GitLab</p>
  <p class="text-sm opacity-65 mt-1 mb-0">Remotes · Merge Requests · Labs 6–7</p>
</div>

<div v-click="4">
  <div class="text-xs font-mono text-amber-600 dark:text-amber-400 font-700">15:45</div>
  <div class="medallion !w-12 !h-12 !mx-0 my-3 bg-amber-500/10"><mdi-lifebuoy class="text-2xl text-amber-600 dark:text-amber-400" /></div>
  <p class="font-700 m-0">Part 4 · Recovery</p>
  <p class="text-sm opacity-65 mt-1 mb-0">Undo cheat-sheet · Lab 8 · drills</p>
</div>

</div>

<div v-click="5" class="mt-8 text-center text-base opacity-80">
Tea breaks at 10:45 and 15:30, lunch at 13:00.
</div>

<!--
- four teaching blocks, each with its own labs; we keep to the clock so nobody is stranded mid-lab at a break
[click] morning starts with the daily loop, Labs 1 and 2
[click] then branching and merging, three labs, including a conflict on purpose
[click] after lunch, GitLab collaboration and the Merge Request flow
[click] last block is the recovery clinic: every undo you will ever need
[click] breaks are real breaks; questions batched there
- ASK: type the number of the block you are most nervous about; I will slow down there
-->
