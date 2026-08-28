# Edge AI Academy

The training system for new Edge AI consultants. It is a Claude Code plugin: an adaptive, mastery-based academy that takes a smart, non-technical new hire from zero to Edge AI Certified, on their own, with no live training time from Alex.

The plugin lives at `plugins/edgeai/`.

## Install (for a new hire)

You need the Claude Code Desktop app installed and signed in. Open a new session and paste this prompt:

```
Please set up Edge AI Academy for me. Run these two commands:

claude plugin marketplace add amart-builder/edge-ai-academy
claude plugin install edgeai@edge-ai-academy --scope user

Then create a folder called Claude on my Desktop with a Projects folder inside it (Desktop/Claude/Projects). That is where all my work will live.

When both are done, tell me to restart the Claude Code app and then type /edgeai:start to begin my training.
```

After the restart, type:

```
/edgeai:start
```

That is the whole entry point. The first run places you and builds your path (about 15 minutes). Every run after that is your daily session, about an hour. `/edgeai:status` shows your progress anytime.

## What certification means

Edge AI Certified is Level 10 (1,800 XP, earned only by demonstrating mastery) plus a passed capstone: a full mock client engagement judged against a rubric. When both land, your scorecard goes to Alex automatically. Then you are ready for client work.

## What's inside

- **Module 1 — How AI Actually Works:** LLMs, how models are made, tokens and context, today's capability frontier (researched live, never stale), where AI is going, how the best companies use it.
- **Module 2 — Claude Code, Our Cockpit:** why it exists, how it works, context and compaction, markdown and CLAUDE.md, skills, memory, working directories, project folder discipline, session hygiene, prompting. Ends with a real build: your own machine, set up the Edge AI way.
- **Module 3 — The Edge AI Method:** the thesis, discovery, scoping, the standard install, the quality bar, client communication. Ends with the capstone: a full mock engagement.

Built by [Edge AI](https://joinedgeai.com).
