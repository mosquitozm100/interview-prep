# Agent Instructions

This repo is an AI-managed interview preparation system.

## Core Rules

1. Always read `CURRENT_STATE.md` before making changes.
2. Keep the repo organized into only three main areas:

   - `behaviour`
   - `coding`
   - `design`

3. Do not create new top-level folders unless explicitly asked.
4. Do not delete old notes. Move or preserve old notes under `archive/old_repo_notes/`.
5. Prefer updating existing tracker files before creating new files.
6. Every coding problem should update `coding/problem_tracker.md`.
7. Every system design topic should update `design/design_tracker.md`.
8. Every behavioural story should update `behaviour/story_bank.md`.
9. Keep notes concise and interview-oriented.
10. At the end of each change, summarize what was updated.

## Writing Style

- Use markdown.
- Prefer tables, checklists, and structured sections.
- Avoid long essays unless explicitly requested.
- Focus on interview usefulness.
- Preserve raw notes when importing from old files.

## Import Rules

- Do not blindly copy old notes into active folders.
- Extract only high-value coding, design, behaviour, and mock feedback items.
- Link back to archived notes when possible.
- Keep uncertain facts marked as `TODO`.
- Do not invent metrics or unsupported accomplishments.

## Daily Update Workflow

When I tell you what I studied today:

1. Read `CURRENT_STATE.md`.
2. Update `DAILY_LOG.md`.
3. Update the relevant tracker:

   - `behaviour/story_bank.md`
   - `coding/problem_tracker.md`
   - `design/design_tracker.md`

4. Update `coding/revisit_list.md` if a coding problem needs repetition.
5. Do not create new files unless the note is substantial.
6. Summarize exactly what changed.

## Weekly Planning Workflow

When asked to create or refresh a weekly plan:

1. Review `DAILY_LOG.md`.
2. Review all three trackers.
3. Pick a realistic weekly plan based on available time.
4. Prefer fewer high-value tasks over many low-value tasks.
5. Update `WEEKLY_PLAN.md`.

## Privacy Rule

Assume this repo may be public. Keep notes sanitized and interview-safe.

## Completion Checklist

Before finishing any task:

- Confirm which files changed.
- Validate tracker formatting if tracker files changed.
- Confirm old notes were preserved.
- Confirm no unnecessary top-level folders were created.
- Make sure modified markdown files are readable in raw form:

  - headings are on separate lines
  - bullets are on separate lines
  - tables have one row per line
  - no major file is compressed into a single huge line

- Summarize the next recommended action.
