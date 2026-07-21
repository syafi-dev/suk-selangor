---
layout: default
transition: slide-up
---

<p class="eyebrow font-mono"><span class="text-purple-600 dark:text-purple-400">part 2</span> &middot; branching &amp; merging</p>

### Common mistakes with branches

<div class="pop grid grid-cols-2 gap-x-14 gap-y-8 mt-8 max-w-4xl mx-auto">

<div v-click="1" class="flex items-start gap-3">
  <mdi-close-circle class="text-2xl pf-cross flex-shrink-0 mt-0.5" />
  <div>
    <p class="font-700 m-0">Committing straight to main</p>
    <p class="text-sm opacity-65 mt-1 mb-1">Skips review and risks breaking shared code.</p>
    <p class="text-sm pf-check m-0"><mdi-check class="inline" /> Branch first, always</p>
  </div>
</div>

<div v-click="2" class="flex items-start gap-3">
  <mdi-close-circle class="text-2xl pf-cross flex-shrink-0 mt-0.5" />
  <div>
    <p class="font-700 m-0">Long-lived branches</p>
    <p class="text-sm opacity-65 mt-1 mb-1">The longer it drifts from main, the uglier the merge.</p>
    <p class="text-sm pf-check m-0"><mdi-check class="inline" /> Merge within days</p>
  </div>
</div>

<div v-click="3" class="flex items-start gap-3">
  <mdi-close-circle class="text-2xl pf-cross flex-shrink-0 mt-0.5" />
  <div>
    <p class="font-700 m-0">Not pulling before merging</p>
    <p class="text-sm opacity-65 mt-1 mb-1">You merge into a stale main and bury fresh work.</p>
    <p class="text-sm pf-check m-0"><mdi-check class="inline" /> Pull main, then merge</p>
  </div>
</div>

<div v-click="4" class="flex items-start gap-3">
  <mdi-close-circle class="text-2xl pf-cross flex-shrink-0 mt-0.5" />
  <div>
    <p class="font-700 m-0">Panicking at conflict markers</p>
    <p class="text-sm opacity-65 mt-1 mb-1">They're instructions, not damage.</p>
    <p class="text-sm pf-check m-0"><mdi-check class="inline" /> Read them, pick, delete</p>
  </div>
</div>

</div>

<!--
[click] committing to main skips review and can break everyone's build; always branch for a change
[click] a branch that lives for weeks drifts far from main and merges painfully; keep them short, days not weeks
[click] merging into a stale main can bury fresh work; pull main right before you merge
[click] conflict markers are instructions; read them, choose the text, delete the markers, done
-->
