# AGENTS.md

This is the operating guide for AI agents maintaining this repository.

## First Rule

Always read [CURRENT_STATE.yaml](CURRENT_STATE.yaml) before making changes.

## Source Of Truth

- Coding problems are tracked in [03_coding/problem_bank.yaml](03_coding/problem_bank.yaml)
- System design topics are tracked in [04_system_design/design_bank.yaml](04_system_design/design_bank.yaml)
- Behavioral stories are tracked in [06_behavioral/story_bank.yaml](06_behavioral/story_bank.yaml)
- Opportunities are tracked in [02_opportunities/pipeline.yaml](02_opportunities/pipeline.yaml)
- Major repo decisions are tracked in [00_control/decision_log.md](00_control/decision_log.md)

Prefer updating the relevant YAML index before creating a new markdown file.

## Content Rules

- Do not overwrite raw notes.
- Do not create too many files.
- Mark AI-generated drafts clearly.
- Preserve original context.
- Mark uncertain facts as `TODO`.
- Do not generate fake accomplishments, fake metrics, or unsupported impact claims.
- Keep interview answers concise and structured.
- When unsure, propose changes in [00_control/decision_log.md](00_control/decision_log.md) instead of editing many files.

## Required Index Updates

- Every coding problem must update `03_coding/problem_bank.yaml`.
- Every system design topic must update `04_system_design/design_bank.yaml`.
- Every behavioral story must update `06_behavioral/story_bank.yaml`.
- Every opportunity must update `02_opportunities/pipeline.yaml`.

## Bilingual Policy

Use English for:

- Directory names
- File names
- YAML keys
- Commit messages
- Interview-facing scripts
- Coding explanation scripts
- System design interview scripts
- Behavioral STAR final answers

Use Chinese for:

- Personal understanding
- Learning notes
- Mistake analysis
- Intuition
- Self-reflection
- Weekly review notes
- Raw thoughts

Important markdown notes should usually follow this structure:

1. 中文理解 / Chinese Understanding
2. English Interview Script
3. Mistakes / 易错点
4. Tradeoffs / 取舍
5. Revisit / 复习状态

## Privacy And Safety

Do not include sensitive immigration, financial, passport, visa, tax, or personal identity documents.

Do not paste confidential company material. Generalize work examples for interview preparation.

## Editing Style

- Keep notes practical and interview-oriented.
- Prefer small updates over broad rewrites.
- Keep status fields current.
- Use `draft`, `todo`, `active`, `revisit`, `done`, and `archived` consistently.
- If importing old material later, copy it into `09_archive/` first and import selectively.
