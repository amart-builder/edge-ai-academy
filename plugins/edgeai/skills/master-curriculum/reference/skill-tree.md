# The Edge AI Consultant Skill Tree

This is the full map of what a new Edge AI consultant must be able to do, taught for a smart person with no technical background. Edge AI is Alex Martin's AI consulting firm: we help businesses implement AI and become AI-native. A certified consultant can explain AI to a business owner without hand-waving, drive Claude Code fluently as their daily cockpit, and run the Edge AI delivery method on a real client.

The `curriculum-architect` agent reads this tree plus the learner's placement, then produces a personalized path. It compresses what the learner already owns and goes deep on the gaps. It never teaches a unit before its prerequisites are mastered.

There are 25 units: 23 teaching units across 3 modules, one applied unit (A1), and one capstone (C1). Each unit has a stable `id` (u1 through u23, a1, c1). Mastery is defined by an observable "can explain or do X" check, never by "understands X." The recurring bar: can you explain this idea to a business owner, in your own words, and can you actually do the thing in your own Claude Code app.

Module keys (used in `learner-profile.json` -> `levels`): `M1-how-ai-works`, `M2-claude-code`, `M3-edge-ai-method`.

---

## The North Star: what "Edge AI Certified" actually means

Not "can recite AI trivia." It means:

1. **Explains AI honestly.** Can tell a business owner what an LLM is, what it can and cannot do, and why, with no hand-waving and no hype.
2. **Drives the cockpit.** Runs Claude Code daily, the Edge AI way: clean folders, a real CLAUDE.md, good sessions, sharp prompts.
3. **Runs the method.** Can take a business from discovery to a scoped proposal to a standard install to a demo, following the Edge AI Method.
4. **Never ships unchecked work.** Verifies everything before it reaches a client. Fresh-eyes review is a reflex, not a step.
5. **Sounds like a person.** Client writing and demos that are clear, human, and never read as AI.

Certification requires Level 10 (1,800 XP) AND passing the C1 capstone. Both. See the learning-engine skill for the certification flow.

---

## Live-research rule (units 4, 6, and 7)

Units u4, u6, and u7 are flagged `live-research: true`. Their content is about the current state of AI, which changes monthly. The `lesson-builder` agent MUST generate these lessons with live web search at teach time, so every example, company story, and statistic is current as of the day it is taught. Never bake dated facts, model names, benchmark numbers, or funding figures into cached lesson material for these units. A lesson taught in March should not cite January's numbers as "right now."

---

## Case bank

Real, sanitized Edge AI client material lives in `reference/case-bank/`. When it has content, lesson-builder pulls examples from it, because learning our real cases doubles as learning our pitch. Until it is populated, lesson-builder uses web-researched examples instead. See `reference/case-bank/README.md`.

---

# MODULE 1: How AI Actually Works `key: M1-how-ai-works`

Goal: a consultant who can explain AI to a business owner without hand-waving. Everything conceptual, nothing requires code or math. Levels 1 to 3.

### u1: What an LLM really is
**The idea:** An LLM (large language model, the kind of AI behind Claude and ChatGPT) is a prediction engine, not a database. It does not look up answers; it predicts the next word, over and over, based on patterns learned from huge amounts of text. Anchor analogy up front: it is like the world's best autocomplete, one that has read most of the internet, not a filing cabinet of facts. This one distinction explains most of what AI gets right and wrong, including why it can sound confident and still be mistaken.
**Mastery check:** Explain to a skeptical business owner what an LLM actually is and why "it's not a database" changes how you should use it. No jargon they would not already know.
**Prereqs:** none.

### u2: How a model gets made
**The idea:** A model goes through stages, and each stage explains something a client will ask about. Pretraining is the read-everything phase, where the model learns language and world patterns from massive text. Fine-tuning is the finishing school, where it learns to be a helpful assistant instead of a raw text predictor. RLHF (reinforcement learning from human feedback, which means humans rating answers so the model learns which ones people prefer) is how it learns manners and judgment. Mastery looks like telling this story in plain English and using it to answer "so does it know about MY business?"
**Mastery check:** Walk through pretraining, fine-tuning, and RLHF in plain words, then use that story to answer a client question like "why doesn't it know our internal pricing?"
**Prereqs:** u1.

### u3: Tokens and context windows
**The idea:** Models do not read words; they read tokens, which are word-chunks (a piece of a word, sometimes a whole one). The context window is the model's working memory: everything it can "see" right now, measured in tokens. When the window fills up, older material falls out or gets squeezed, like a whiteboard that runs out of space. This is a fundamentals concept that Module 2 applies daily: it is why long sessions drift, why we manage context on purpose, and why "just paste everything in" is not a strategy.
**Mastery check:** Explain tokens and the context window with the whiteboard analogy, then predict what happens to a conversation that far outgrows the window and why.
**Prereqs:** u1.

### u4: The capability frontier right now `live-research: true`
**The idea:** What today's best models can actually do, this month, with real examples. This is the "insane current capabilities" unit: agents that work for hours, models that see and hear, code written end to end, real business workflows running on AI. The lesson-builder researches this live at teach time so every example is current; nothing here is allowed to go stale. Mastery looks like a consultant who can name current, concrete capabilities to a client without exaggerating or underselling.
**Mastery check:** Give a business owner three current, concrete examples of what frontier AI can do this month, each one real and verifiable, and honestly name one thing it still cannot do reliably.
**Prereqs:** u1, u2.

### u5: Where AI is going
**The idea:** The consensus view of the next few years: models keep getting more capable, agents do more real work with less supervision, and the cost of a unit of intelligence keeps falling. Just as important: where smart people disagree (how fast, what breaks, which jobs change first), so the consultant can hold an honest position instead of parroting hype or doom. Mastery looks like giving a client a grounded two-minute view of the future with clear labels on what is consensus and what is contested.
**Mastery check:** Give the two-minute "where this is going" answer, clearly separating what most experts agree on from where they split, without hype in either direction.
**Prereqs:** u4.

### u6: How the best companies use AI `live-research: true`
**The idea:** Real companies, real workflows, real results: how the best operators actually use AI today, from solo founders to enterprises. Live-researched at teach time so the examples are current, plus our own sanitized client wins from the case bank as they land. This unit doubles as sales training: every example the learner masters is a story they can tell a prospect.
**Mastery check:** Tell three current company stories of AI use (what they did, how, what changed), at least one relevant to a small or mid-size business, ready to retell to a prospect.
**Prereqs:** u4.

### u7: AI by the numbers `live-research: true`
**The idea:** The current stats and figures that paint the picture: adoption rates, spend, productivity findings, market size, whatever numbers best tell the story this month. Live-researched at teach time; a stat from six months ago is a liability in a client meeting. Mastery looks like a consultant who has five or six current numbers at their fingertips and knows where each one comes from.
**Mastery check:** Recall five current AI statistics with their sources, and use two of them to make the case for AI adoption to a specific kind of business.
**Prereqs:** u4.

---

# MODULE 2: Claude Code, Our Cockpit `key: M2-claude-code`

Goal: a fluent daily driver of the Claude Code Desktop app, set up the Edge AI way. Everything hands-on: each unit has the learner doing it in their own app, not reading about it. Levels 4 to 7.

### u8: Why Claude Code exists + first session
**The idea:** Claude Code is our cockpit: one app where you talk to a top AI that can also read files, write files, and run real work on your computer, not just chat. This unit gets it installed, oriented, and used: the learner has their first real working conversation and does something genuinely useful in it. Mastery looks like comfort, not expertise: they open it without dread and get real work out of a session.
**Mastery check:** Install Claude Code, run a first session, and complete one real small task in it (for example, have it read a file and summarize it), then describe what happened in plain words.
**Prereqs:** u3.

### u9: How it works on the backend
**The idea:** Behind the chat is the agent loop: the model reads your request, picks a tool (read a file, run a command, search), looks at the result, and repeats until done. Permissions are the guardrails: Claude asks before doing anything risky, and you decide. Think of it like a skilled contractor in your house: capable of real work, but they knock before entering a room. Knowing this loop turns "it's magic" into "I know roughly what it is doing and why it paused to ask me."
**Mastery check:** Explain the agent loop (model, tools, permissions) with an analogy, and correctly predict why Claude paused to ask permission in a given scenario.
**Prereqs:** u8.

### u10: Context in practice
**The idea:** Module 1 taught what a context window is; this unit is living with one. Long sessions fill the window, and a bloated context makes Claude slower, dumber, and more expensive. Compaction is the fix: the session gets summarized down so the important parts stay and the noise goes, and we autocompact at 400k tokens the Edge AI way. Mastery looks like a driver who notices context bloat, knows what compaction will and will not preserve, and starts fresh when that is the better move.
**Mastery check:** Explain why we autocompact at 400k tokens, what compaction keeps and loses, and name two signs that a session's context has gotten bloated.
**Prereqs:** u8, u3.

### u11: Markdown and CLAUDE.md
**The idea:** Markdown is the plain-text formatting language AI reads and writes natively (headers with #, lists with -, simple and readable). CLAUDE.md is a special markdown file Claude Code reads at the start of every session: your standing instructions, like a briefing memo a new assistant reads every morning before work. In this unit the learner writes their own real CLAUDE.md: who they are, their role at Edge AI, their voice, their rules. This file is graded again in A1.
**Mastery check:** Write your own working CLAUDE.md (identity, role, voice, rules) in clean markdown, and explain what Claude does with it and why it beats repeating yourself every session.
**Prereqs:** u8.

### u12: Skills
**The idea:** A skill is a packaged playbook Claude can load and follow: a set of instructions for one kind of task, written once and reused forever, like a recipe card in a shared kitchen. Edge AI runs on skills, and clients get ours as part of an install. This unit covers what skills are, how to invoke the ones we ship, and the anatomy of one (the description that triggers it, the instructions inside), so the learner can use them and explain them.
**Mastery check:** Invoke a skill in your own session, then open its file and walk through its anatomy: what triggers it, what it tells Claude to do, and why a skill beats retyping instructions.
**Prereqs:** u11.

### u13: Memory
**The idea:** Claude's memory carries selected facts across sessions, so it remembers decisions and preferences without being retold. The judgment call is what belongs there: durable decisions, corrections, and preferences go in; routine progress and one-off details stay out. Think of it as the difference between what you would write in a company handbook and what you would leave in yesterday's meeting notes. Mastery looks like a driver who saves the right things and keeps memory from becoming a junk drawer.
**Mastery check:** Given six candidate items from a work session, correctly sort what should be saved to memory versus not, and defend each call.
**Prereqs:** u8.

### u14: The working directory
**The idea:** Every Claude Code session runs inside one folder, the working directory: that folder is Claude's desk for the session, and everything it reads and writes starts from there. Picking it deliberately is the difference between a focused session and a confused one. Start a session in the project's folder and Claude finds the right files, the right CLAUDE.md, the right context; start in the wrong place and it flails.
**Mastery check:** Explain what the working directory is, start two sessions in different project folders on purpose, and say what changed between them and why it matters.
**Prereqs:** u8.

### u15: Claude > Projects discipline
**The idea:** The standard Edge AI folder layout: a Claude > Projects folder tree, one folder per project, and a STATUS.md file in each. STATUS.md is the project's living one-page brief: the goal, the rules, what is done, what is next, so any session (or any person) can pick the project up cold. This discipline is what keeps AI-driven work organized instead of scattered across a hundred chats. The learner builds their own tree in this unit and it is graded in A1.
**Mastery check:** Build your own Claude > Projects tree with at least one real project folder containing a proper STATUS.md, and explain what each part of STATUS.md is for.
**Prereqs:** u14.

### u16: Session hygiene
**The idea:** When to start a new session versus staying in the current one. Stay while the work is one continuous task and the context is earning its keep; start fresh when switching projects, when the context is bloated, or when you want clean eyes on a review. A session is like a meeting: one topic per meeting beats one endless meeting about everything. Mastery is making this call correctly by habit.
**Mastery check:** Given four scenarios, correctly call stay versus new session for each and give the reason in one sentence.
**Prereqs:** u10, u14.

### u17: Prompting that works
**The idea:** Specs over vibes: the difference between "make it better" and telling Claude what you want, what done looks like, and what to avoid. Great prompting is mostly great specification, plus the habit of iterating on results instead of accepting the first draft. This unit is hands-on: the learner rewrites weak prompts into strong ones and watches the output quality move.
**Mastery check:** Take a vague request, rewrite it as a sharp prompt (goal, context, what done looks like), run both in your own session, and articulate why the outputs differ.
**Prereqs:** u8, u11.

### a1: APPLIED: Set up your machine (75 XP)
**The idea:** The applied milestone for Module 2. The learner sets up their own machine the Edge AI way, for real: the Claude > Projects folder tree exists, their personal CLAUDE.md is written and loaded, and their first real project folder exists with a proper STATUS.md. This is not an exercise; it is the setup they will actually work in from now on. The evaluator grades it against a checklist.
**Mastery check (evaluator-judged, against the A1 checklist):** (1) Claude > Projects folder tree exists and is sane. (2) A personal CLAUDE.md is written (identity, role, voice, rules) and in the right place. (3) A first real project folder exists with a STATUS.md covering goal, rules, done, and next.
**Prereqs:** u11, u15, u17.

---

# MODULE 3: The Edge AI Method `key: M3-edge-ai-method`

Goal: can run our delivery method on a real client. Levels 8 to 10.

**Alignment note (applies to every unit in this module):** The Edge AI Method HTML is the single source of truth for the method. When it ships, the content of units u18 through u23 must align to its actual sections, and lessons should reference it rather than restate it. Until then, teach at the level of coverage written here and do not invent proprietary method details that the HTML has not defined.

### u18: The Edge AI thesis
**The idea:** What Edge AI sells and why it works: we make businesses AI-native, meaning AI is wired into how the business actually operates day to day, not bolted on as a chatbot experiment. The consultant must be able to state the thesis in one minute, define "AI-native" in terms a client cares about (speed, cost, capability), and explain why now. Content aligns to the Edge AI Method HTML when it ships.
**Mastery check:** Deliver the one-minute Edge AI thesis to a cold prospect, including a plain definition of "AI-native" and why acting now beats waiting.
**Prereqs:** u7, u17 (Module 1 complete and prompting fluency).

### u19: Discovery
**The idea:** Auditing a business for AI leverage: where the hours go, where the bottlenecks are, what work is repetitive and rule-shaped versus judgment-shaped, and reading the org (who wants this, who fears it, who decides) before proposing anything. Good discovery is mostly listening and looking, not pitching. Content aligns to the Edge AI Method HTML when it ships.
**Mastery check:** Given a description of a real-feeling business, produce a discovery findings summary: top AI leverage points, the org read, and the questions you would still need answered.
**Prereqs:** u18.

### u20: Scoping and proposals
**The idea:** Turning discovery findings into a scoped, priced engagement: what we will do, in what order, for what outcome, at what price, with a clear line around what is not included. A good scope protects both sides; a vague one guarantees a bad project. Content aligns to the Edge AI Method HTML when it ships.
**Mastery check:** Turn a set of discovery findings into a one-page scoped proposal: deliverables, sequence, outcome, price logic, and explicit exclusions.
**Prereqs:** u19.

### u21: The standard install
**The idea:** What we actually set up for clients: Claude Code, configuration, the folder discipline, skills, and memory, the same system the learner built for themselves in Module 2 and A1, adapted to a client's business. The consultant can name every piece of the install, what it is for, and roughly how it goes in. Content aligns to the Edge AI Method HTML when it ships.
**Mastery check:** Write an install plan for a specific client: every component of the standard install, what each is for in their business, and the order you would set them up.
**Prereqs:** u20, a1.

### u22: The quality bar
**The idea:** Verify before shipping, always. Nothing reaches a client unchecked: work gets a fresh-eyes AI review (a clean session with no memory of writing it, reviewing it cold), and the consultant personally confirms the result does what it claims. The rule is absolute because one unchecked error costs more trust than a hundred good deliverables earn. Content aligns to the Edge AI Method HTML when it ships.
**Mastery check:** Take a plausible AI-produced deliverable containing planted flaws, run the verification process on it, catch the flaws, and state the never-ship-unchecked rule and why it is absolute.
**Prereqs:** u21.

### u23: Client communication
**The idea:** Teaching the client, running demos, and writing that does not sound like AI. Clients buy confidence and clarity: short sentences, plain words, real terms defined on first use, and absolutely no AI tells in anything they receive. A demo is a story with a payoff, not a feature tour. Content aligns to the Edge AI Method HTML when it ships.
**Mastery check:** Write a short client-facing update and a five-minute demo script for an install; both must be clear, human, and free of AI tells, judged against the voice rules.
**Prereqs:** u21.

### c1: CAPSTONE: Mock engagement (75 XP, required for certification)
**The idea:** The full method, run end to end on a fictional business: discovery, then a scoped proposal, then an install plan, then a demo script. This is the certification gate. The evaluator judges the whole package against the mock-engagement rubric; passing it plus Level 10 (1,800 XP) makes the learner Edge AI Certified and triggers the scorecard to Alex (see the learning-engine skill).
**Mastery check (evaluator-judged, against the C1 rubric):** A complete mock engagement package: (1) discovery findings, (2) a scoped proposal, (3) an install plan, (4) a demo script. Each piece must meet the bar of its source unit, hang together as one coherent engagement, and read as client-ready.
**Prereqs:** u19, u20, u21, u22, u23.

---

## The prerequisite graph

```
M1:  u1 ─> u2 ─> u4 ─> u5
     u1 ─> u3           u4 ─> u6
                        u4 ─> u7
M2:  (u3) ─> u8 ─> u9
             u8 ─> u10 ──┐
             u8 ─> u14 ──┴─> u16     (u16 needs u10 and u14)
             u8 ─> u13
             u14 ─> u15
             u8 ─> u11 ─> u12
             u8, u11 ─> u17
     (u11, u15, u17) ─> a1
M3:  (u7, u17) ─> u18 ─> u19 ─> u20 ──┐
                                  a1 ──┴─> u21 ─> u22     (u21 needs u20 and a1)
                                        u21 ─> u23
     (u19, u20, u21, u22, u23) ─> c1
```

A unit is `available` when all its listed prereqs are `mastered`. The modules are broadly sequential (finish Module 1's core before Module 2 opens fully, Module 2 plus A1 before Module 3's install units), but within a module the graph allows parallel branches so sessions can interleave.

---

## XP map (must sum with the engine's rules)

- 23 teaching units at 50 XP each = 1,150.
- A1 (75) + C1 (75) = 150.
- Spaced reviews across the run at 10 XP each land roughly 150 to 250.
- First-try bonuses at 25 XP each land roughly 150 to 350.

Honest completion lands at 1,800+, which is Level 10. A learner who struggles still gets there through reviews. Nobody gets there without the capstone.

---

## Compression rules for the architect

Placement scores the learner 0 to 5 per module (`M1-how-ai-works`, `M2-claude-code`, `M3-edge-ai-method`). Expect most new hires to place at 0 to 1 across the board; that is normal and fine, and the path is built for it. Apply per module:

- Module at level 4 or 5: replace each of its units with a quick confirmation check. Passing the confirmation counts as mastering the unit and awards its full XP (plus the +25 first-try bonus when passed on the first attempt), so placement never costs a learner XP on the road to 1,800.
- Module at level 3: teach only the gaps in full; confirmation-check the rest (same XP rule).
- Module at level 0 to 2: full teaching, every unit.
- A1 and C1 are never compressed or skipped. Every learner does them for real, on their own machine and their own mock engagement. C1 is required for certification no matter what.
- Units u4, u6, and u7 are never served from cache. Even a confirmed-out learner sees current material if these are re-taught as reviews.
- Never place a unit before its prereqs. Compression means cutting what the learner already owns, never lowering the mastery bar.
