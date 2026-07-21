---
layout: default
transition: slide-left
---

<p class="eyebrow font-mono"><span class="text-blue-600 dark:text-blue-400">part 3</span> &middot; gitlab collaboration</p>

### What GitLab is

<p class="text-sm opacity-60 mt-1 mb-6">A place to host your repos and collaborate: Merge Requests, issues, CI/CD, all in one.</p>

<div class="grid grid-cols-2 gap-8 max-w-4xl mx-auto">

<div v-click="1" class="flex items-start gap-4">
  <div class="medallion !w-14 !h-14 !mx-0 bg-blue-500/10 flex-shrink-0"><mdi-server-security class="text-3xl text-blue-600 dark:text-blue-400" /></div>
  <div>
    <p class="font-700 text-lg m-0">Self-hosted</p>
    <p class="text-sm opacity-70 mt-1 mb-1">Runs on your own servers.</p>
    <p class="text-sm m-0"><code>git.selangor.gov.my</code> — data stays in-house, full control.</p>
  </div>
</div>

<div v-click="2" class="flex items-start gap-4">
  <div class="medallion !w-14 !h-14 !mx-0 bg-green-500/10 flex-shrink-0"><mdi-cloud-outline class="text-3xl text-green-600 dark:text-green-400" /></div>
  <div>
    <p class="font-700 text-lg m-0">SaaS</p>
    <p class="text-sm opacity-70 mt-1 mb-1">Hosted &amp; managed by GitLab.</p>
    <p class="text-sm m-0"><code>gitlab.com</code> — nothing to maintain, sign up and go.</p>
  </div>
</div>

</div>

<div v-click="3" class="mt-10 text-center text-base opacity-80">
GitLab, GitHub and Bitbucket are the same idea — we use <span class="text-blue-600 dark:text-blue-400 font-600">self-hosted GitLab</span> here.
</div>

<!--
- GitLab is the shared home for your repositories, plus the tools around them: reviews, issues, automated tests
[click] self-hosted means it runs on the state's own servers, like git.selangor.gov.my; the code and data stay in-house, which matters for government
[click] SaaS means GitLab runs it for you at gitlab.com; nothing to maintain, but the data lives with them
[click] GitHub and Bitbucket are the same category of tool; the daily commands you learned do not change between them; we are on self-hosted GitLab today
- gloss: self-hosted vs SaaS is like owning your office building versus renting a serviced office
-->
