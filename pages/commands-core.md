---
layout: default
transition: slide-left
---

### Commands worth knowing cold

<div class="term-print max-w-3xl mx-auto mt-6">
<TermWindow title="the core eight">
<div class="grid grid-cols-2 gap-x-10">
  <div v-click="1" class="py-1"><span class="text-amber-300 font-700 inline-block w-40">git clone &lt;url&gt;</span><span class="text-gray-400">copy a repo down</span></div>
  <div v-click="1" class="py-1"><span class="text-amber-300 font-700 inline-block w-40">git status</span><span class="text-gray-400">what changed &amp; where</span></div>
  <div v-click="2" class="py-1"><span class="text-amber-300 font-700 inline-block w-40">git add &lt;file&gt;</span><span class="text-gray-400">stage changes</span></div>
  <div v-click="2" class="py-1"><span class="text-amber-300 font-700 inline-block w-40">git commit -m</span><span class="text-gray-400">save a snapshot</span></div>
  <div v-click="3" class="py-1"><span class="text-amber-300 font-700 inline-block w-40">git pull</span><span class="text-gray-400">fetch + merge others'</span></div>
  <div v-click="3" class="py-1"><span class="text-amber-300 font-700 inline-block w-40">git push</span><span class="text-gray-400">send commits up</span></div>
  <div v-click="4" class="py-1"><span class="text-amber-300 font-700 inline-block w-40">git log --oneline</span><span class="text-gray-400">history, compact</span></div>
  <div v-click="4" class="py-1"><span class="text-amber-300 font-700 inline-block w-40">git diff</span><span class="text-gray-400">exactly what changed</span></div>
</div>
</TermWindow>
</div>

<div v-click="5" class="mark-safe mt-8 text-center text-lg opacity-85">
Nobody memorises these — <span v-mark="{ at: 5, color: '#dc2626', type: 'underline' }">screenshot this one</span>.
</div>

<!--
- the whole day runs on these eight; every one starts with the word git
[click] clone copies a remote repo to your machine; status answers "what changed since my last save?"
[click] add picks what to save next; commit takes the snapshot with a message
[click] pull brings others' work down; push sends yours up
[click] log lists the history compactly; diff shows the exact edited lines
[click] reassure like a driving instructor: look them up for a week and your fingers learn them; screenshot this slide
- gloss: diff is the "track changes" view; log is the document's revision history
-->
