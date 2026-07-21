---
layout: default
transition: slide-left
---

### Every block, the same rhythm

<div class="pop grid grid-cols-4 gap-4 mt-14 max-w-4xl mx-auto text-center">

<div v-click="1">
  <div class="medallion bg-cyan-500/10"><mdi-book-open-variant class="text-3xl text-cyan-600 dark:text-cyan-400" /></div>
  <p class="font-700 mt-3 mb-0">Recap</p>
  <p class="text-xs font-mono opacity-50 mt-1 mb-1">3–5 min</p>
  <p class="text-sm opacity-65 m-0">The concept and the commands.</p>
</div>

<div v-click="2">
  <div class="medallion bg-red-500/10"><mdi-test-tube class="text-3xl text-red-600 dark:text-red-400" /></div>
  <p class="font-700 mt-3 mb-0">Lab</p>
  <p class="text-xs font-mono opacity-50 mt-1 mb-1">15–25 min</p>
  <p class="text-sm opacity-65 m-0">You run it yourself.</p>
</div>

<div v-click="3">
  <div class="medallion bg-amber-500/10"><mdi-alert class="text-3xl text-amber-600 dark:text-amber-400" /></div>
  <p class="font-700 mt-3 mb-0">Pitfall</p>
  <p class="text-xs font-mono opacity-50 mt-1 mb-1">5 min</p>
  <p class="text-sm opacity-65 m-0">The mistakes people hit.</p>
</div>

<div v-click="4">
  <div class="medallion bg-green-500/10"><mdi-account-group class="text-3xl text-green-600 dark:text-green-400" /></div>
  <p class="font-700 mt-3 mb-0">Debrief</p>
  <p class="text-xs font-mono opacity-50 mt-1 mb-1">5 min</p>
  <p class="text-sm opacity-65 m-0">Compare notes, lock it in.</p>
</div>

</div>

<div v-click="5" class="mark-safe mt-14 text-center text-lg opacity-85">
Type every command yourself, <span v-mark="{ at: 5, color: '#dc2626', type: 'underline' }">don't just watch</span>.
</div>

<!--
- the shape repeats all day, so after block one you know exactly what is coming
[click] recap is short: refresh the idea and the commands, no long theory
[click] the lab is the point; you type it on the shared practice repo, not me
[click] then the pitfalls: the specific mistakes people hit right here, and how to dodge them
[click] debrief: we compare what happened, clear questions, and move on
[click] muscle memory is the whole reason for a refresher; typing beats watching every time
- gloss: like a driving lesson, you learn by driving, not by watching someone describe the pedals
-->
