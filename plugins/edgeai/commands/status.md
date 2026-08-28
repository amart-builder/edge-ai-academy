---
description: "Show your Edge AI Academy dashboard: rank, level, XP, streak, mastered units, what's due for review, and what's next. Read-only."
allowed-tools: Read, Glob, Grep, Bash
---

# Edge AI Academy: Dashboard

Show the learner a clean, motivating snapshot of where they are. Read-only: do not change any state.

## Do this

1. Resolve `STATE_DIR` by running `echo "${EDGEAI_ACADEMY_STATE:-$HOME/EdgeAI-Academy}"`. Read from `STATE_DIR`:
   - `progress.json` (xp, level, rank, certified, streak, badges, history)
   - `curriculum.json` (units and statuses, spaced-rep `nextReview` dates)
   - `learner-profile.json` (goal, preferences)
   If `learner-profile.json` is missing, tell them they have not started yet and to run `/edgeai:start` to begin. Stop.

2. Compute from the data:
   - Path progress: `unitsMastered / totalUnits`.
   - Due reviews: units where `spacedRep.nextReview <= today`.
   - Next available unit: the first unit with status `available`.
   - Rank and next rank from these XP thresholds: New Hire 0, Operator 400, Builder 900, AI-Native Consultant 1400, Edge AI Certified 1800. Level = `floor(xp / 200) + 1`. (These thresholds and the level formula mirror learning-engine SKILL.md; if they ever differ, that file is authoritative.) Show "Edge AI Certified" as the rank only if `certified` is true in `progress.json`; at 1,800+ XP without a passed capstone, show "AI-Native Consultant" and note that the C1 capstone is what remains.
   - For the XP bar, show progress within the current rank: fill = `min(1, (xp - currentRankFloor) / (nextRankFloor - currentRankFloor))` (never overfill past 100%, even at 1,800+ XP while C1 is pending), and label it `<xp> XP (<nextRankFloor - xp> to <nextRank>)`. If certified, show the bar full.

3. Render a dashboard like this (fill with real values, keep the ASCII bars honest):

```
╭─ EDGE AI ACADEMY ────────────────────────────────────────╮
   Jordan · Rank: Operator · Level 3 · 🔥 4-day streak

   XP    ███████████░░░░░░░░░  450 XP (450 to Builder)
   Path  █████░░░░░░░░░░░░░░░  6 / 25 units mastered (24%)

   Goal: Edge AI Certified.
╰───────────────────────────────────────────────────────────╯

📅 Due for review today (3)
   • u1: What an LLM really is
   • u3: Tokens and context windows
   • u8: Why Claude Code exists + first session

🎯 Up next
   • u10: Context in practice

🏅 Badges: first-blood, plain-talker

▸ Type /edgeai:start to start today's session.
```

4. Adjust to their vibe preference: if `minimal`, drop the XP/streak/badge lines and show just path progress, due reviews, and next up. If `full-game`, lean into the celebration. If `certified` is true, lead with that and show reviews plus the offer to refresh a live-research unit.

5. One honest, specific line of encouragement based on their recent history (from `progress.json` -> `history`). No filler, no em dashes, seventh-grade reading level.

Keep it to one screen. This is a glance, not a report.
