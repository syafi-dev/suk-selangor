---
layout: default
transition: slide-left
---

<p class="eyebrow font-mono"><span class="text-red-600 dark:text-red-400">part 1</span> &middot; git core refresher</p>

### What Git actually is

<div class="grid grid-cols-2 gap-8 mt-6 items-stretch">

<div v-motion :initial="{ x: -40, opacity: 0 }" :enter="{ x: 0, opacity: 1, transition: { type: 'spring', stiffness: 90, delay: 150 } }">
<div class="from-left rounded-xl overflow-hidden border border-gray-400/40 shadow-lg bg-gray-100 text-gray-700 h-full">
  <div class="flex items-center gap-1.5 px-4 py-2.5 bg-gray-200 border-b border-gray-300">
    <span class="w-3 h-3 rounded-full bg-red-400"></span>
    <span class="w-3 h-3 rounded-full bg-yellow-400"></span>
    <span class="w-3 h-3 rounded-full bg-green-400"></span>
    <span class="ml-3 text-xs text-gray-500">Folder — without Git</span>
  </div>
  <div class="px-5 py-4 space-y-2.5 text-sm font-mono">
    <div v-click="1" class="flex items-center gap-2"><mdi-file-document-outline class="text-gray-400" /> report.docx</div>
    <div v-click="1" class="flex items-center gap-2"><mdi-file-document-outline class="text-gray-400" /> report-final.docx</div>
    <div v-click="1" class="flex items-center gap-2"><mdi-file-document-outline class="text-gray-400" /> report-final-v2.docx</div>
    <div v-click="1" class="flex items-center gap-2"><mdi-file-document-outline class="text-gray-400" /> report-FINAL-fix.docx</div>
    <div v-click="1" class="flex items-center gap-2 text-red-500"><mdi-help-circle-outline /> which one is real?</div>
  </div>
</div>
</div>

<div v-motion :initial="{ x: 40, opacity: 0 }" :enter="{ x: 0, opacity: 1, transition: { type: 'spring', stiffness: 90, delay: 150 } }">
<div class="from-right h-full term-print">
<TermWindow title="one file, full history — with Git">
<div v-click="2"><span class="text-green-400">$</span> git log --oneline</div>
<div v-click="2" class="text-amber-300">a1b9c2e <span class="text-gray-400">Fix login redirect</span></div>
<div v-click="3" class="text-amber-300">7f3d0aa <span class="text-gray-400">Add opening hours</span></div>
<div v-click="3" class="text-amber-300">c04e11b <span class="text-gray-400">Add menu section</span></div>
<div v-click="4" class="text-amber-300">e5a7d90 <span class="text-gray-400">First draft</span></div>
</TermWindow>
</div>
</div>

</div>

<div v-click="4" class="mark-safe mt-8 text-center text-lg opacity-85">
Git keeps <span v-mark="{ at: 4, color: '#dc2626', type: 'underline' }">every version</span> of one file, with a note on each.
</div>

<!--
- version control is the whole idea; Git is the tool everyone uses for it
[click] the familiar mess: one document saved five times with worse and worse names; nobody knows which is current
[click] with Git it stays one file, and the history lives beside it; log lists every saved version, newest on top
[click] each line is a snapshot with a short message saying what changed and why
[click] so nothing is ever lost and you can always see how the file got here
- gloss: a commit is a labelled snapshot, like a photo in a gallery with a caption; the log is the album
- STORY: land = naming files "final" never scales. Pick a real time a "final_v2" mix-up cost rework; ordinary setup, the pain, the cost, how one history ends it. 60-90s.
-->
