---
layout: default
transition: slide-left
---

### Resolving a conflict, step by step

<div class="grid grid-cols-2 gap-8 items-center mt-4">

<div class="pop space-y-3">
  <div v-click="1" class="step-row items-center"><span class="step-num">1</span><span><b>Pull &amp; see the flag</b> <span class="opacity-60">· git pull names the files</span></span></div>
  <div v-click="2" class="step-row items-center"><span class="step-num">2</span><span><b>Open the file</b> <span class="opacity-60">· find &lt;&lt;&lt; === &gt;&gt;&gt;</span></span></div>
  <div v-click="3" class="step-row items-center"><span class="step-num">3</span><span><b>Choose the final text</b> <span class="opacity-60">· keep one, the other, or blend</span></span></div>
  <div v-click="4" class="step-row items-center"><span class="step-num">4</span><span><b>Delete the markers</b> <span class="opacity-60">· remove all three lines</span></span></div>
  <div v-click="5" class="step-row items-center"><span class="step-num">5</span><span><b>Stage &amp; commit</b> <span class="opacity-60">· git add, then git commit</span></span></div>
</div>

<div class="term-print">
<TermWindow title="resolve">
<div v-click="1"><span class="text-green-400">$</span> git pull</div>
<div v-click="1" class="text-amber-300"># CONFLICT (content): app.js</div>
<div v-click="3" class="opacity-50"># ...fix the file by hand...</div>
<div v-click="5"><span class="text-green-400">$</span> git add app.js</div>
<div v-click="5"><span class="text-green-400">$</span> git commit</div>
<div v-click="5" class="text-green-400"># done, conflict resolved</div>
</TermWindow>
</div>

</div>

<div v-click="6" class="mt-6 flex items-center justify-center gap-2 caution text-base">
  <mdi-lifebuoy /> Stuck? <code>git merge --abort</code> rewinds you to before the merge. Nothing is lost.
</div>

<!--
[click] pull tells you exactly which files conflict; it does the flagging for you
[click] open the file and find the three marker lines
[click] edit so the file reads the way it should; keep yours, theirs, or a blend of both
[click] delete all three marker lines completely, or Git will not accept it
[click] add the file and commit to finish the merge
[click] if it feels tangled, merge --abort takes you right back to before you pulled; breathe and retry
- gloss: the markers are like tracked-changes bubbles you resolve, then delete the bubbles
-->
