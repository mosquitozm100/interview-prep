# LLM Eval Platform

## Problem Statement

Design a platform for evaluating model or agent quality across datasets, versions, and workflows.

## Requirements

- Store eval datasets and test cases.
- Run evals against model or agent versions.
- Support automatic grading and human review.
- Compare results across runs.
- Capture traces for debugging.
- TODO: Define target eval types.

## Core Entities

- Dataset
- Test case
- Eval run
- Model / agent version
- Grader
- Result
- Trace
- Human review

## API / Interface

- `POST /eval_runs`
- `GET /eval_runs/{id}`
- `GET /eval_runs/{id}/results`
- `POST /datasets`

## High-Level Architecture

- Control plane manages datasets and run configs.
- Job queue schedules eval execution.
- Workers call models, agents, and graders.
- Result store supports comparison and dashboards.
- Review queue handles ambiguous cases.

## Key Flows

- User creates eval run.
- Workers execute test cases.
- Graders score outputs.
- Results are aggregated and compared with baseline.

## Scaling / Reliability

- Run evals asynchronously.
- Version datasets and graders.
- Capture traces for reproducibility.
- Use sampling or prioritization for expensive runs.

## Observability

- Eval run latency
- Cost per run
- Pass/fail by category
- Grader disagreement rate
- Regression alerts

## Tradeoffs

- Automated graders scale but can be noisy.
- Human review improves quality but adds latency and cost.

## Interview Summary

I would frame the eval platform as a versioned experiment system that runs async jobs, captures traces, applies graders, and compares results over time to catch regressions.
