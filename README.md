# Career Interview OS

This repository is an AI-managed interview preparation operating system for 2026 backend, AI backend, LLM evals, and agent workflow roles.

It is designed to answer three questions every day:

1. What should I study today?
2. What are my current weak areas?
3. If I had an interview tomorrow, what coding problems, system designs, and behavioral stories should I review?

## Why This Exists

Interview prep can easily become a pile of notes. This repo is meant to be a source of truth: indexes track status, markdown files hold understanding and scripts, and daily/weekly logs turn prep into a repeatable loop.

Current target areas:

- Backend SWE roles with strong system design expectations
- AI backend and agent infrastructure roles
- LLM eval platform and support automation roles
- OpenAI-style backend/evals/support automation engineering roles

## Daily Use

Start with [CURRENT_STATE.yaml](CURRENT_STATE.yaml), then choose one focused session:

- Coding: solve or revisit one problem and update [03_coding/problem_bank.yaml](03_coding/problem_bank.yaml)
- System design: review one design or one fundamental and update [04_system_design/design_bank.yaml](04_system_design/design_bank.yaml)
- Behavioral: refine one story and update [06_behavioral/story_bank.yaml](06_behavioral/story_bank.yaml)

Log what happened in [DAILY_LOG.md](DAILY_LOG.md). Keep notes short, honest, and useful.

## Weekly Use

Use [WEEKLY_PLAN.md](WEEKLY_PLAN.md) and the weekly review template to:

- Review weak areas
- Move items into or out of the revisit queue
- Pick next week's coding, system design, and behavioral focus
- Update active opportunities in [02_opportunities/pipeline.yaml](02_opportunities/pipeline.yaml)

## How AI Agents Should Help

AI agents should maintain structure, not create clutter. Always read [AGENTS.md](AGENTS.md) and [CURRENT_STATE.yaml](CURRENT_STATE.yaml) first.

Good AI help includes:

- Updating YAML indexes after each prep session
- Turning raw Chinese notes into concise English interview scripts
- Flagging weak areas and next actions
- Keeping drafts clearly marked
- Avoiding unsupported metrics or fake accomplishments

The repo should help thinking happen naturally in Chinese while making interview answers crisp in English.
