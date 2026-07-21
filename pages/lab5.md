---
layout: default
transition: slide-left
---

<Lab :n="5" title="Create & resolve a merge conflict" goal="Deliberately cause a conflict, then fix it, so it becomes routine, not scary." caution="Do this twice and swap roles. The goal is that conflicts stop feeling like emergencies.">

<li v-click="1" class="step-row"><span class="step-num">1</span><span>In pairs: both edit the <b>same line</b> of <code>conflict.txt</code>.</span></li>
<li v-click="2" class="step-row"><span class="step-num">2</span><span>Partner A commits &amp; pushes first.</span></li>
<li v-click="3" class="step-row"><span class="step-num">3</span><span>Partner B commits, then tries to push (rejected).</span></li>
<li v-click="4" class="step-row"><span class="step-num">4</span><span>Partner B runs <code>git pull</code>, and the conflict appears.</span></li>
<li v-click="5" class="step-row"><span class="step-num">5</span><span>Edit the file, remove markers, add, commit, push.</span></li>

<template #terminal>
<TermWindow title="your turn — Partner B">
<div v-click="4" class="opacity-50"># after the rejected push:</div>
<div v-click="4"><span class="text-green-400">$</span> git pull</div>
<div v-click="4" class="text-amber-300"># CONFLICT in conflict.txt</div>
<div v-click="5" class="opacity-50"># ...edit, remove &lt;&lt;&lt; === &gt;&gt;&gt;...</div>
<div v-click="5"><span class="text-green-400">$</span> git add conflict.txt</div>
<div v-click="5"><span class="text-green-400">$</span> git commit -m "Resolve conflict"</div>
<div v-click="5"><span class="text-green-400">$</span> git push</div>
</TermWindow>
</template>

</Lab>

<!--
- we cause a conflict on purpose; doing it deliberately is how it stops being scary
[click] pair up and both edit the very same line, so a clash is guaranteed
[click] Partner A pushes first and wins the race
[click] Partner B's push is rejected because B is now behind
[click] B pulls and Git flags the conflict inside conflict.txt
[click] B edits to the final wording, deletes the markers, adds, commits, pushes
- then swap roles and do it again; second time it should feel routine
- ACTIVITY: after resolving, both partners refresh GitLab together to confirm one clean final line
-->
