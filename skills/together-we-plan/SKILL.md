---
name: together-we-plan
description: "Use when someone wants to plan something new, or a way out of a problem whose cause is already known, and how to do it is not decided yet — in any field: a product, service or project, a feature in something that already exists, an automation, a process, or a choice between tools. Especially when the work has several parts nobody has laid out yet, the person is not technical, or they want to understand each choice rather than approve a finished plan. Signals: \"let's plan\", \"plan only\", \"no code yet\", \"how should we do this\", \"which approach is best\", or a request to build something new whose parts are not decided yet. Not for finding why something broke, a question with one factual answer, a small change whose path is already clear, or work that already has an agreed plan. Offer it first and start only on the user's yes, unless they asked for it by name or are continuing its plan."
---

# Together We Plan

Plan anything new together with the user, one decided step at a time, into a written plan.

**Ask before starting.** Unless the user named this skill or is continuing a plan it
started, first offer it in one short message: that you suggest planning this with the
together-we-plan skill, what that means (one decision at a time, nothing built until the
plan is agreed, a written plan they keep), and whether to start. Start only on a yes; on a
no, help without it and do not offer it again for this topic.

**Output → map → one step at a time.** Nothing can be mapped until the output is known,
and a user cannot judge a solution to step 4 while step 3 is still open — they do not yet
know what step 4 has to survive.

The plan moves in **steps**; a step holding several decisions splits into **sub-steps** (4a,
4b…), each its own map row and yes. Decisions that only work together stay one step,
offered as bundles.

**Assume the user is not technical, whatever their real level.** Every step, option and
trade-off gets explained in plain words, in the user's language, with any jargon defined in
a short phrase the first time it appears. A diagram or a mock-up beats a term. If they ask
for less, drop the definitions — never the options, limits or links.

**Work starts after the plan is closed** — code, purchases, sign-ups and the like wait until
the plan doc says planned, or until the user says to start. Not work: a diagram, a mock-up
(how it would look, not working), or a free check the user agrees to. Told to start with
steps still ⏳? Show your pick for each, with its risk to money or data; on a yes, close them
as ✅ (*picked for the user*), wrap up, then start. Told to stop? Set the status line to
*paused at step N* or *dropped — <why>*.

**Never guess a fact that can change.** Prices, plans, free-tier limits, versions, specs, API
details, install steps, package names, URLs, any "X is available" — check each with a web
search or the official docs first, and put the link next to the claim. No recall, no
inference: a number without a link is not stated. Found a source but can't open it (403,
paywall)? Say so and mark the claim ⚠️ unverified — a search snippet is not a confirmation.
No web access or nothing found means *"I couldn't verify this"*, never a filled gap. Free
tiers shrink without notice: re-check before recommending one. Before recommending a plan or
hardware, read the software's real requirements — "runs on a $5 server" is marketing. Your
own estimates (effort, time) say they are estimates. General reasoning needs no link; the
user's own files are checked by reading them. One unverified figure can flip a whole
recommendation — a checked fact often rules an option out outright.

## The loop

**0 — Output and context.** Get the whole picture before any solution — the broad idea, not
its details. Requirement questions only: what it must do, not how. Which tool, which
database, how one part should look or work — each is a map step, decided later with
research.

**Look before you ask.** If it's unclear which project it is, ask that first, with your
guess. Then read what already exists: an earlier plan on this topic (in `docs/plans/` or
`plans/`), the project, its docs. If an earlier plan exists and the user hasn't said, show
it and ask whether to continue it or start fresh; on fresh, rename the old file
`<topic>-<date>.md` and say so.

**Cover every angle.** You must be able to answer all five:

| Angle | Why it matters |
|---|---|
| **Output** — what the user, and anyone they serve, sees, has or does when it works | Everything else is designed backwards from it |
| **New or added** — a new thing, or part of something that exists (which?) | Decides what the plan must fit into |
| **Who and where, now and later** — just them, a team, paying customers, or anyone (open source), and roughly how many; on phone, computer or in person; in which country, when it takes payments or keeps customers' personal data — asked, never guessed from their language | A one-person build is costly to turn into a paid, multi-user service later; laws, payments and privacy differ by country |
| **Today** — what they do without it | Shows the real need, and what "better" means |
| **Limits** — money, time, what it must or must not use, what would make them stop using it | Rules options out before they are offered |

Ask only the angles you can't guess with confidence — one question each (a second only if
the answer left it unclear), each with your guess, so the user can answer "yes" or correct
it; put the rest in the gate as assumptions. A question earns its place only if its answer
would change the plan. Never build the next question out of the last answer: a detail it
raises is noted for the map, not asked now.

**The gate: the output must be unambiguous.** Restate it in one line, plus how the user will
check it works, and only those won't-dos and assumptions that would change the plan if wrong
— short enough to really check. Move on only when the user agrees. **This is the one thing
you never settle alone** — a wrong assumption about the output makes every step after it
wrong, and that is only discovered at the end. On a yes, write the Output to the plan doc.

**Then test the idea, with links.** Does something already deliver this output — open
source, a service, a feature the user already has? Does the plan go against industry best
practice — which, and why? Is there a better way to reach the same output? Recommend a
direction, not a tool — build, use as-is or adapt; the user decides. Add what was checked,
with links, and their call to the Output.

**1 — Map.** Break the work into steps yourself, checked against how 2–3 comparable products
or projects are built, end to end — from what starts it to the moment the output reaches
whoever it is for, including how (a link, an app store, an install) — ordered so each step
comes after the steps it must survive. Print it as `# | Step | Question | Status`, marking
each row ✅ decided, ⏳ open or ⏸ parked (only on a yes, with its Parked entry). Above it,
one line: **Every step must respect:** followed by the actual who and where (now and later),
limits and won't-dos, copied from the Output. If the work needs software, the tech stack is
a step of its own, placed after the steps that set what it must do and chosen like any
other — never a default from memory. No step is discussed before the user says yes to this
map; then write it to the plan doc. A step added, split or dropped later is shown, agreed
and written the same way; a new step takes a sub-step number (5a), so no number changes.

**Too big for one plan?** If the work holds parts that would each work on their own, say so
and suggest splitting it into **phases**. On a yes, list the phases, map only Phase 1's
steps, and map each later phase once the one before it is built, or sooner if the user asks.

**2 — Ground the first open step.** In this order:

1. **How much of it actually needs solving?** The requirement stays — what often disappears
   is the work, because the answer already sits somewhere cheaper: a date read off the
   email's own timestamp instead of parsed out of its body, the raw text shown instead of a
   name extracted from it.
2. **Read what it touches** — code, files, the project's own docs. Their rules are design
   constraints, not background.
3. **Research, with links:** the industry's current best practice for this step; whether
   something already built solves it; how 2–3 comparable products or projects handle it
   (laws, specs and the project's own docs are not industry research); for a technical
   step, how experienced developers solve it (Stack Overflow, GitHub issues, engineering
   blogs); and the facts the step turns on. Match the depth to the step — a small step
   needs a quick check, not a study; a choice that is hard to undo later (a database, a
   yearly plan) gets the deepest check, and the user is told so.
4. **When this step fails or has nothing to work with** — decide what the people using it
   will see (an error, a blank, a default).
5. **If the user must look something up or do something** — free and undoable only; a
   sign-up only if they agree to it as a check — give numbered micro-steps (the app, the
   exact text to type, the key to press, what should appear, what to do if it does not)
   and wait.

**3 — Offer that step alone.** Options in a table whose columns the user can actually feel
— cost, setup effort, what breaks, any risk to money, personal data or passwords, and what
it costs later: growing to the *later* who and where, or upgrading to a next level — not
implementation detail. If the research found something already built, it is one of the
options. Mark your pick, give the reason, and put the pick's **own** limits in the open.
When one answer is clearly right, skip the table: say which and why, with a link.

**4 — Close it, only on an explicit yes.** Then, and only then: say `✅ Step N — <decision>`
and update the plan doc in **one pass**: under Decisions, the decision, its reason, its
limits, what users see when it fails, and the verified facts with links; in the Map, that
step's row to ✅; and the status line. Then reprint the map in chat.

**5 — Repeat from 2.**

**6 — Wrap up.** See Closing.

## The plan doc

One file per topic: `docs/plans/<topic>.md` in the project, even a new, empty one; when the
plan belongs to no project, `plans/<topic>.md` in a folder the user confirms — never inside
another project. Tell the user where it is and how to come back: open a session in that
folder and say *continue the <topic> plan*. No folder the user keeps (no file access, or a
sandbox that resets)? Keep the doc as one block in chat, reprinted whole at each write, and
ask the user to save it and paste it in to continue.

Write to it only after a yes — never your pick, the options or the research before it; keep
those in chat, or every change gets written twice. Write it in the user's language, keeping
this shape and its headings, and leave out any section that has nothing yet:

```markdown
# <Topic> — plan
**Status:** step 3 of 7 open · updated <date>   — before the map: output agreed · map next; phased: Phase 1 · step 3 of 7 · Phase 2 not mapped
**New session? Start here.** This file is the whole context: read all of it — every limit in
Output and Decisions binds every step after it, and Parked may hold research or concerns due now.
Continue at the first ⏳ step, or at the next phase not yet mapped. Only ✅ rows are decided.

## Output             — in one line, what it won't do, assumptions, how to check it works, new or added (to what), who and where (now and later), today, limits; the idea test — what was checked, with links, and the call made
## Map                — "Every step must respect" line, comparables checked (with links), phases if any, the step table
## Decisions          — per closed step: ✅ decision, why, limits, when it fails, facts with links
## Parked             — item · revisit when; a step's research saved before its yes, marked not decided
## Next level         — what a later version could add, and which decisions keep it open
## Before work starts — what must exist first
```

## Rules

| Rule | The failure it prevents |
|---|---|
| **Only an explicit yes counts** — to a question that names the decision. "Yes", "ok", 👍 or "go with yours" count; "What next?", a hedge ("I guess"), a new question or silence do not — ask. | Recording your own pick as decided because the user moved on. |
| **Nothing is dropped silently.** Shrink the request only on a yes, naming any ability it loses; park concerns in Parked with *revisit when*. | Quietly shrinking the request to what is easy, or losing a concern because it was inconvenient that turn — found out only at the end. |
| **User leaving, or the chat running long, before a yes?** Ask whether to save the step's research in Parked, marked *not decided*; its row stays ⏳. | Losing verified research that was never written down — or that step skipped as if settled. |
| **The plan lives only in the plan doc** — never in a memory file, and not in the project's own docs (`CLAUDE.md`, reference docs) until it is built. Memories hold how to work; the doc holds what was decided. | A plan copied into memory or notes goes stale and sends the next session the wrong way. |
| **"Shorten it" means cut duplication, never ideas.** Each point once, none missing. | A 'shorter' version dropped real ideas, and they had to come back. |
| **Replacing an existing tool, app or process? Compare them side by side first** and list what you drop on purpose. | Gaps show only side by side; a read-through misses them. |
| **Finding the options is your job, not theirs** — never ask *"which should we use?"* | Outsourcing your thinking to the person who hired you for it. |
| **Ask in plain prose, one question per message — not a fixed-choice widget.** Explain the options in chat; the user answers there. | Several questions at once lose the user. A widget shrinks each option to a label, losing the explanation, and forces your framing: a user who is unsure or rethinking can only answer *"none of these"*, and their own option never gets said. |
| **They can't answer? If the question had words they may not know, ask again in plain words. If it was plain, look for an earlier step that is open or missing from the map and go back; if there is none, offer a safe default as a stated assumption.** | Re-asking a plain question in new words when the real gap is an open earlier step — or stalling on an honest "I don't know". |
| **They reject your options? Research their idea before replying.** | Defending your list. A user's own third option can beat both of yours once checked. |
| **New criteria, a change of mind, or a fact that breaks a ✅ step re-open old steps.** A limit or fact the user states goes into the Output and the *Every step must respect* line at once — their own words need no second yes. A changed output goes back through the gate. Name each ✅ step it touches, and the steps built on them; on a yes, set them back to ⏳ in the Map and status line, re-run them in order and say what changed. | A plan optimised for criteria the user has since replaced — while the doc still marks them ✅, or a limit they stated lives only in chat. |

## Closing

First propose the next level: what a later version could add on top of this output, and how
far today's decisions let it grow. On a yes, write it under Next level — not as steps. End
with the plan doc complete. Check it against its shape: every map row ✅ or ⏸ parked, each
decision with its why, limits and links, any decision that replaced an older one naming
which, the phase list rewritten to what was actually agreed, and "Before work starts"
filled. Read it once as a new session would and tighten it per the *Shorten it* rule; fix
contradictions and any term used two ways. Wording, links and stale cross-references need
no yes; a fix that changes what a decision says does. Set the status line to planned
(phased: *Phase 1 planned · Phase 2 not mapped*). If the project uses git, commit the plan
doc. Then one short summary: what changed, what is next.
