---
layout: default
transition: slide-left
---

### The everyday cycle

<p class="text-sm opacity-60 mt-1 mb-4">This loop is 90% of your Git use.</p>

<div class="grid grid-cols-2 gap-8 items-center">

<div class="pop space-y-3">
  <div v-click="1" class="step-row items-center"><span class="step-num">1</span><span><b>git pull</b> <span class="opacity-60">· get the latest before you start</span></span></div>
  <div v-click="2" class="step-row items-center"><span class="step-num">2</span><span><b>edit</b> <span class="opacity-60">· do your actual work</span></span></div>
  <div v-click="3" class="step-row items-center"><span class="step-num">3</span><span><b>git add</b> <span class="opacity-60">· stage what's ready</span></span></div>
  <div v-click="4" class="step-row items-center"><span class="step-num">4</span><span><b>git commit</b> <span class="opacity-60">· save a snapshot + message</span></span></div>
  <div v-click="5" class="step-row items-center"><span class="step-num">5</span><span><b>git push</b> <span class="opacity-60">· share it back to GitLab</span></span></div>
  <div v-click="6" class="flex items-center gap-2 text-sm opacity-70 pl-1"><mdi-refresh class="text-cyan-600 dark:text-cyan-400" /> then loop back to <code>git pull</code> to stay in sync</div>
</div>

<div class="term-print">
<TermWindow title="the loop">
<div v-click="1"><span class="text-green-400">$</span> git pull <span class="opacity-40"># start from the latest</span></div>
<div v-click="3"><span class="text-green-400">$</span> git add index.html <span class="opacity-40"># git add . = everything</span></div>
<div v-click="4"><span class="text-green-400">$</span> git commit -m "Fix header spacing"</div>
<div v-click="5"><span class="text-green-400">$</span> git push <span class="opacity-40"># share with the team</span></div>
</TermWindow>
</div>

</div>

<!--
- this is the rhythm of a normal working day; five steps, then repeat
[click] pull first, always: you start from everyone else's latest work, not yesterday's copy
[click] then edit, the real work, same as ever
[click] add stages what is ready; you choose, it is not automatic
[click] commit saves a snapshot with a message that says what and why
[click] push shares it back so the team sees it
[click] then loop: pull often through the day so you never drift far from main
- ASK: type 1 if you usually pull before you start, 2 if you forget; the forgetters cause most conflicts, gently
-->
