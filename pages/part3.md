---
layout: default
transition: slide-up
---

<div class="h-full flex flex-col justify-center relative">

<div class="absolute right-6 top-1/2 -translate-y-1/2 part-numeral select-none pointer-events-none">3</div>

<p class="eyebrow font-mono"><span class="text-blue-600 dark:text-blue-400">part 3</span> &middot; gitlab collaboration</p>

<div v-motion :initial="{ x: -20, opacity: 0 }" :enter="{ x: 0, opacity: 1, transition: { type: 'spring', stiffness: 90, delay: 100 } }">

# GitLab collaboration

</div>

<div v-motion :initial="{ opacity: 0 }" :enter="{ opacity: 1, transition: { delay: 450, duration: 500 } }" class="mt-4 text-xl opacity-70 max-w-xl">
Remotes, Merge Requests, and reviewing each other's work the GitLab way.
</div>

</div>

<!--
- this block moves from your machine to the team; GitLab is where the shared work and the reviews live
- we cover what GitLab is, remotes and origin, then the Merge Request flow, with two roleplay labs
- gloss: if Git is the camera, GitLab is the shared photo album everyone can see and comment on
-->
