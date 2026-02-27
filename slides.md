---
theme: default
title: How to Get More Out of AI (As a Human)
colorSchema: dark
transition: slide-left
drawings:
  persist: false
---

# How to Get More Out of AI

## (As a Human)

---

# The Two Types of Work

<div class="grid grid-cols-2 gap-12 mt-8">
<div>

### High Touch
*Needs your attention*

- Lots of comments & feedback expected
- Requires iteration after AI's first attempt
- Might just be garbage

</div>
<div>

### Low Touch
*Set and forget*

- Likely to get LGTM straight away
- Minor feedback only
- Variable names, frontend copy, etc.

</div>
</div>

<!--
When you're working with AI, not all tasks are created equal. Some need you closely involved the whole time. Others you can fire off and barely think about until the PR is up.
-->

---

# High Touch — Indicators

<v-clicks>

- **No strong patterns** — old services with mixed patterns
- **Complicated flows** — like change of ownership
- **Hairy side effects** — proximity to centre of the graph
  - e.g. teams vs notes
- **Novel work** — novel overall, or novel to you
  - Results in not-so-good prompting
- **High quality bar** — you really want it to be very, very good

</v-clicks>

<!--
These are the signals that a task will need your close attention. The AI will struggle with ambiguity, mixed patterns, and complicated flows — so you need to be there to guide it.
-->

---

# Low Touch — Indicators

<v-clicks>

- **Small expected code change size**
- **Very strong patterns** — or good examples to copy
- **Library upgrades**
- **Repetitive work** — same shape, different names

</v-clicks>

<!--
These are the tasks where AI shines with minimal guidance. Strong patterns and clear examples mean the AI can often get it right on the first try.
-->

---

# The Bottleneck

<div class="mt-12 text-center">

Each high-touch task demands your **cognitive attention** —

reviewing, iterating, course-correcting.

<div class="text-3xl mt-8 font-bold">

You can only run so many in parallel<br>before getting overwhelmed.

</div>

</div>

<!--
This is the key insight. Even if AI is doing the coding, high-touch tasks still consume your mental bandwidth. You're the bottleneck, not the AI. So the question becomes: how do we move tasks from high-touch to low-touch?
-->

---
layout: center
---

# So how do we move tasks<br>from high to low touch?

---

# Approach 1: Skills via Human Iteration

<v-clicks>

1. Tell Claude you're developing a **reusable skill** for XYZ
2. Go through all the steps to produce the skill
3. Run it, check the output
4. Feed back mistakes, ask for updates
5. Repeat

</v-clicks>

<div v-click class="mt-6 p-4 border border-gray-600 rounded">

**Example:** Feature toggle skill

**Trade-off:** Burns lots of tokens, slow cycle time — but it works.

</div>

<!--
This is the most manual approach. You're essentially pair-programming with the AI to build a reusable skill. It's slow and expensive, but you end up with something that other engineers can use too.
-->

---

# Approach 2: Skills via AI Iteration with Exemplar

Give the AI an **exemplar endpoint** to learn from.

<div class="mt-8 text-xl italic text-gray-400">

"AI cheated by checking the answers"

</div>

<v-clicks>

- Faster cycle time than Approach 1
- AI compares its output against the known-good example
- Self-corrects without your involvement

</v-clicks>

<!--
Instead of you being in the feedback loop, the AI can compare its own output against a working example. It's like giving a student the answer key — they can check their own work. This dramatically speeds up the iteration cycle.
-->

---

# Approach 3: Copy Exemplar PRs

The simplest approach.

<div class="text-2xl mt-8 mb-8">

Point at a PR and say **"do this again for X."**

</div>

<v-clicks>

- Similar to Approach 2, but without creating a reusable skill
- Great for one-off or infrequent tasks
- Works surprisingly well when patterns are clear

</v-clicks>

<!--
Sometimes you don't need a skill. If there's a good PR that does what you want, just tell the AI to replicate it. No abstraction needed. This is the pragmatic choice for tasks you won't repeat often.
-->

---

# Approach 4: Strong Patterns (Long-term)

Services drift over time as we develop better ideas.

<v-clicks>

With AI, it's no longer unreasonable to **bring entire services in line with new patterns**.

Do it incrementally — like library upgrades,<br>the longer you leave it the more painful it gets.

</v-clicks>

<div v-click class="mt-8 text-gray-400 italic">

Unverified, but promising.

</div>

<!--
This is the long-term vision. Historically, we've accepted that services will have inconsistent patterns because the cost of alignment was too high. AI changes that equation. If we keep patterns strong and consistent, almost everything becomes low-touch.
-->

---

# What This Unlocks

<div class="grid grid-cols-2 gap-12 mt-8">
<div>

### Stream 1: High Touch
Your focused attention.

One task at a time, guiding AI through complexity.

</div>
<div>

### Stream 2: Low Touch
AI works, you review.

Multiple tasks in flight — check in when PRs are ready.

</div>
</div>

<div v-click class="mt-8 p-4 border border-gray-600 rounded text-center">

Speculative work becomes viable — things that aren't needed *right now* but might be needed in the future.

</div>

<!--
With enough low-touch tasks, you can maintain two permanent streams of work. Your high-touch stream gets your focus, while low-touch tasks tick along in the background. And because low-touch tasks are cheap to run, you can even take on speculative work — things that would never have been prioritised before because the effort couldn't be justified.
-->

---

# Bonus Tips

<v-clicks>

- **Time your prompts around breaks**
  - Fire one off before lunch, before EOD
  - The implementation phase takes the longest (comes after brainstorming check-ins)
  - Don't fire the *initial* prompt before a break — it'll barely have started when you get back
- **Don't always use AI**
  - Know when it's faster to just do it yourself

</v-clicks>

<!--
A couple of practical tips. Timing matters — you want the AI working while you're away, but make sure it's past the initial back-and-forth phase first. And sometimes the right answer is to not use AI at all. If you can do something in 5 minutes, the overhead of prompting and reviewing isn't worth it.
-->

---
layout: center
---

# Questions?
