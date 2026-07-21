---
layout: default
transition: slide-left
---

### .gitignore: keep junk out of history

<p class="text-sm opacity-60 mt-1 mb-4">A <code>.gitignore</code> lists what Git should never track: dependencies, build output, secrets, OS clutter. Add it before your first commit.</p>

<div class="grid grid-cols-2 gap-8 items-start">

<div class="term-print">
<TermWindow title=".gitignore">
<div v-click="1" class="opacity-50"># dependencies</div>
<div v-click="1">node_modules/</div>
<div v-click="1">vendor/</div>
<div v-click="2" class="opacity-50"># secrets — never commit these</div>
<div v-click="2" class="text-red-400">.env</div>
<div v-click="2" class="text-red-400">*.key</div>
<div v-click="3" class="opacity-50"># build &amp; OS files</div>
<div v-click="3">dist/</div>
<div v-click="3">.DS_Store</div>
</TermWindow>
</div>

<div class="space-y-5">
  <div v-click="4" class="caution flex items-start gap-2">
    <mdi-alert class="flex-shrink-0 mt-0.5" />
    <span><b>Already committed a secret?</b> Adding it to <code>.gitignore</code> does NOT remove it from past commits. Treat it as leaked: rotate the key now, then scrub history with an admin.</span>
  </div>
  <div v-click="5" class="term-print">
    <TermWindow title="untrack something already committed">
      <div><span class="text-green-400">$</span> git rm -r --cached node_modules</div>
      <div><span class="text-green-400">$</span> echo "node_modules/" &gt;&gt; .gitignore</div>
      <div><span class="text-green-400">$</span> git commit -m "Stop tracking deps"</div>
    </TermWindow>
  </div>
</div>

</div>

<!--
[click] list your dependency folders; they are huge and rebuildable, never commit them
[click] secrets are the important one: .env files, private keys; if these reach history they are exposed to everyone with the repo
[click] build output and OS files like .DS_Store are noise; ignore them too
[click] the trap: if you already committed a secret, ignoring it now does nothing to the past commits; the secret is still in history, so treat it as leaked, rotate it immediately, then have an admin scrub history with filter-repo or BFG
[click] to stop tracking something already committed, rm --cached removes it from Git but keeps your local copy, then commit
- gloss: .gitignore is a "do not photograph" list the camera checks before every snapshot
-->
