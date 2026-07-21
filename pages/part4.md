---
layout: default
transition: slide-up
---

<div class="h-full flex flex-col justify-center relative">

<div class="absolute right-6 top-1/2 -translate-y-1/2 part-numeral select-none pointer-events-none">4</div>

<p class="eyebrow font-mono"><span class="text-amber-600 dark:text-amber-400">part 4</span> &middot; oops! recovery clinic</p>

<div v-motion :initial="{ x: -20, opacity: 0 }" :enter="{ x: 0, opacity: 1, transition: { type: 'spring', stiffness: 90, delay: 100 } }">

# Oops! Recovery clinic

</div>

<div v-motion :initial="{ opacity: 0 }" :enter="{ opacity: 1, transition: { delay: 450, duration: 500 } }" class="mt-4 text-xl opacity-70 max-w-xl">
Almost every mistake in Git is reversible. Here's how to undo the common ones, calmly.
</div>

</div>

<!--
- the last block turns fear into a checklist; nearly nothing in Git is truly lost
- we cover the undo cheat sheet, two classic rescues, a symptom-to-fix table, then a drills lab
- the golden rule we keep repeating: when it feels messy, STOP and ask before piling on more commands
-->
