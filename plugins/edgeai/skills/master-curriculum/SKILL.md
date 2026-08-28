---
name: master-curriculum
description: "The master skill tree for becoming an Edge AI Certified consultant, and the rules for compiling it into a personalized curriculum. Use when designing or revising a learner's path, deciding what to teach next, or checking what a unit requires. Read by the curriculum-architect agent and the academy daily loop."
version: 1.0.0
---

# Master Curriculum

This skill holds the complete map of what an Edge AI consultant must be able to do, plus the rules for turning that map into one learner's personalized path. The audience is smart, non-technical new hires at Edge AI, Alex Martin's AI consulting firm.

## The two jobs this skill supports

1. **Compile a curriculum.** Given a learner's assessed levels and preferences, produce an ordered list of units that goes from where they are to Edge AI Certified, compressing what they own and going deep on gaps.
2. **Answer "what's next" and "what does this need."** During daily learning, resolve prerequisites and pick the next unit.

## How to use it

The full tree lives in `reference/skill-tree.md`. Always read it before compiling or revising a curriculum. It defines:
- All 25 units (u1 to u23, a1, c1) across the three modules, with module `key`s that match `learner-profile.json` -> `levels`.
- What each unit covers and why it matters for a working consultant.
- Observable "can do X" mastery checks (never "understands X").
- The prerequisite graph and the XP map.
- The compression rules, including the units that can never be skipped (A1 and C1).
- The live-research flag on u4, u6, and u7 (these lessons are built with live web search at teach time, never from cached facts).
- The Module 3 alignment note (the Edge AI Method HTML is the source of truth for units u18 to u23 once it ships).

## The non-negotiables

- **Mastery is observable.** A unit is mastered only when the learner can demonstrate the check, not when they say they get it.
- **Prereqs are real.** Never schedule a unit before its prerequisites are mastered.
- **A1 and C1 are sacred.** Every learner does the applied machine setup and the capstone mock engagement for real. C1 gates certification, always.
- **Compress redundancy, never rigor.** Skipping a unit the learner already owns (via a passed confirmation check, which still awards its XP) is good. Skipping a true prerequisite builds a consultant who looks competent and collapses in front of a client.
- **Hands-on beats reading.** Module 2 units happen in the learner's own Claude Code app. Module 3 units produce real artifacts (findings, proposals, plans, scripts).
- **Current beats cached.** The live-research units (u4, u6, u7) are always taught from fresh web research.

The output format for a compiled curriculum is defined in the learning-engine state schema (`curriculum.json`). The `curriculum-architect` agent produces it.
