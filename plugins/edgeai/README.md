# Edge AI Academy

The adaptive, mastery-based training system every new Edge AI consultant completes on their own, entirely inside Claude Code. Edge AI is Alex Martin's AI consulting firm; this academy takes a smart, non-technical new hire from wherever they start to Edge AI Certified, with zero live training time from Alex.

It places your real level (most people start near zero, and the path is built for that), builds a personalized curriculum, and teaches with the learning methods that actually work fast: mastery learning, active recall, spaced repetition, deliberate practice, and learning by teaching. You never advance past something until you can actually do it, and you never sit through what you already know.

## The path

- **Module 1: How AI Actually Works.** Explain AI to a business owner without hand-waving. The current-capabilities, company-examples, and stats units are researched live at teach time, so they are never stale.
- **Module 2: Claude Code, Our Cockpit.** Become a fluent daily driver of Claude Code, set up the Edge AI way. Every unit is hands-on in your own app, and it ends with A1: setting up your real machine, graded for real.
- **Module 3: The Edge AI Method.** Run our delivery method: thesis, discovery, scoping, the standard install, the quality bar, client communication. It ends with C1, the capstone: a full mock engagement, judged against a rubric.

Certification is Level 10 (1,800 XP) plus a passed capstone. Both. When you get there, your scorecard goes to Alex automatically.

## Install

Edge AI Academy is a Claude Code plugin. From your terminal:

```bash
# Placeholder until the GitHub repo exists; your onboarding doc has the current command.
claude plugin marketplace add <edge-ai-academy marketplace source>
claude plugin install edgeai@edge-ai-academy
```

Restart Claude Code so the plugin loads, then run `/edgeai:start`. (Plugin commands are namespaced, so it is `/edgeai:start`, not a bare `/edgeai`.)

## How to use

- `/edgeai:start`: the one command you need. First time, it places you and builds your path. After that, it runs your daily session. Shortcuts: `/edgeai:start review`, `/edgeai:start next`, `/edgeai:start reassess`, `/edgeai:start settings`.
- `/edgeai:status`: a quick glance at your rank, XP, streak, what is due for review, and what is next.

A learning session happens in a single Claude Code session and is fully interactive. Your progress is saved between sessions, so you pick up exactly where you left off. A session is about an hour; most people finish the whole path in a few weeks of dailies.

## What's inside

**Commands** (what you type)
- `/edgeai:start`: the coach and router. Onboards you, then runs daily mastery-paced sessions, then runs certification when you earn it.
- `/edgeai:status`: the dashboard.

**Agents** (the non-interactive staff the coach delegates to)
- `assessor`: designs your placement and grades it, gently. Built for beginners.
- `curriculum-architect`: compiles your personalized, dependency-ordered path.
- `lesson-builder`: authors each unit's lesson, tuned to you. Uses live web search for the units about current AI capabilities, companies, and stats.
- `evaluator`: grades your mastery checks, your machine setup (A1), and your capstone (C1), honestly.

**Skills** (the brains)
- `learning-engine`: the teaching method: the loop, mastery gates, spaced repetition, gamification, the audience and voice rules, and the certification sequence. Includes the state schema.
- `master-curriculum`: the Edge AI consultant skill tree (all 25 units) and the rules for compiling it into your path. Includes the case bank folder for sanitized client examples.

## Where your progress lives

`~/EdgeAI-Academy/`
- `learner-profile.json`: who you are, your level per module, your preferences.
- `curriculum.json` / `curriculum.md`: your path (machine and human-readable).
- `progress.json`: XP, level, rank, streak, badges, certification.
- `scorecard.md`: written at certification; this is what goes to Alex.
- `sessions/`: a short journal per learning day.

This is separate from the plugin code, so updating or reinstalling the plugin never touches your progress. Set the `EDGEAI_ACADEMY_STATE` environment variable to store it somewhere else.

## Design notes

- The main Claude Code session is your live coach. It does all the talking and adapts in real time. It spawns the agents above for the heavy lifting (designing, planning, authoring, grading) to keep the conversation sharp.
- Mastery is always observable: "can do X," never "understands X." Compression comes from confirming what you already own, never from lowering the bar.
- The learner-facing voice is a training ground for the client-facing voice: plain, human, seventh-grade reading level, every term defined with an analogy, and never an em dash or en dash anywhere.
- Module 3 content aligns to the Edge AI Method HTML (the single source of truth for the method) as it ships.
