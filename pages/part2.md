---
layout: default
transition: slide-up
---

<div class="h-full flex flex-col justify-center relative">

<div class="absolute right-6 top-1/2 -translate-y-1/2 part-numeral select-none pointer-events-none">2</div>

<p class="eyebrow font-mono"><span class="text-purple-600 dark:text-purple-400">part 2</span> &middot; branching &amp; merging</p>

<div v-motion :initial="{ x: -20, opacity: 0 }" :enter="{ x: 0, opacity: 1, transition: { type: 'spring', stiffness: 90, delay: 100 } }">

# Branching & merging

</div>

<div v-motion :initial="{ opacity: 0 }" :enter="{ opacity: 1, transition: { delay: 450, duration: 500 } }" class="mt-4 text-xl opacity-70 max-w-xl">
Work in parallel without stepping on each other, and resolve conflicts calmly.
</div>

</div>

<!--
- this block is where teams stop clobbering each other's work; branches make parallel work safe
- we cover what a branch really is, the two merge shapes, then three labs including a conflict on purpose
- STORY: land = a conflict is normal, not a disaster. Pick a time two people edited the same file; the pain of the rejected push, then how reading the markers resolved it in a minute. 60-90s.
-->
