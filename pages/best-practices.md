---
layout: default
transition: slide-up
---

<p class="eyebrow font-mono"><span class="text-blue-600 dark:text-blue-400">part 3</span> &middot; gitlab collaboration</p>

### Habits that keep collaboration smooth

<div class="pop grid grid-cols-3 gap-x-10 gap-y-5 mt-6 max-w-4xl mx-auto text-center">

<div v-click="1">
  <div class="medallion !w-14 !h-14 bg-blue-500/10"><mdi-package-variant-closed class="text-2xl text-blue-600 dark:text-blue-400" /></div>
  <p class="font-700 mt-2 mb-1">Keep MRs small</p>
  <p class="text-sm opacity-65 m-0">One change each — easy to revert.</p>
</div>

<div v-click="1">
  <div class="medallion !w-14 !h-14 bg-blue-500/10"><mdi-text-box-outline class="text-2xl text-blue-600 dark:text-blue-400" /></div>
  <p class="font-700 mt-2 mb-1">Write a real description</p>
  <p class="text-sm opacity-65 m-0">What changed, why, how to test.</p>
</div>

<div v-click="2">
  <div class="medallion !w-14 !h-14 bg-blue-500/10"><mdi-link-variant class="text-2xl text-blue-600 dark:text-blue-400" /></div>
  <p class="font-700 mt-2 mb-1">Link the issue</p>
  <p class="text-sm opacity-65 m-0">Reference #number, stays traceable.</p>
</div>

<div v-click="2">
  <div class="medallion !w-14 !h-14 bg-green-500/10"><mdi-refresh class="text-2xl text-green-600 dark:text-green-400" /></div>
  <p class="font-700 mt-2 mb-1">Pull main daily</p>
  <p class="text-sm opacity-65 m-0">Small merges beat one big one.</p>
</div>

<div v-click="3">
  <div class="medallion !w-14 !h-14 bg-green-500/10"><mdi-eye-check-outline class="text-2xl text-green-600 dark:text-green-400" /></div>
  <p class="font-700 mt-2 mb-1">Review kindly, fast</p>
  <p class="text-sm opacity-65 m-0">A stalled MR blocks a teammate.</p>
</div>

<div v-click="3">
  <div class="medallion !w-14 !h-14 bg-green-500/10"><mdi-broom class="text-2xl text-green-600 dark:text-green-400" /></div>
  <p class="font-700 mt-2 mb-1">Delete merged branches</p>
  <p class="text-sm opacity-65 m-0">Keep the branch list clean.</p>
</div>

</div>

<!--
[click] one change per MR, and a description that says what, why, and how to test; reviewers can then actually review it
[click] link the issue number so anyone can trace why a change exists; pull main daily so your branch never drifts far
[click] review other people's MRs quickly and kindly; a sitting MR blocks a colleague; delete branches once merged so the list stays readable
- these six habits are what separates a smooth team from a tangled repo
-->
