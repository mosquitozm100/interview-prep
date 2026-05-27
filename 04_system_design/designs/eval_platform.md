# LLM Eval Platform

## 中文理解

Eval platform 是 AI 系统的质量闭环。它管理数据集、运行实验、调用模型/agent、打分、人工复核、结果分析和回归监控。

## Requirements

- Store eval datasets and test cases.
- Run evaluations against model or agent versions.
- Support automatic and human grading.
- Compare runs over time.
- Surface regressions and failure examples.

## APIs

- `POST /eval_runs`
- `GET /eval_runs/{id}`
- `POST /datasets`
- `GET /results?run_id=...`

## Data Model

- Dataset
- Test case
- Eval run
- Model or agent version
- Grader
- Result
- Human review

## High-Level Design

- Control plane manages datasets and run config.
- Job queue schedules eval execution.
- Workers call models/agents and graders.
- Results store supports analysis and dashboards.
- Review workflow handles ambiguous or high-risk failures.

## Deep Dives

- Dataset versioning.
- Metric definitions.
- Reproducibility.
- Human-in-the-loop review.
- Trace capture for debugging.

## Bottlenecks

- Model call cost and latency.
- Large result storage.
- Grader reliability.
- Dataset quality.

## Tradeoffs / 取舍

- Automated graders scale but may be noisy.
- Human review is higher quality but slower and more expensive.
- Offline batch evals are reproducible; online evals catch production drift.

## Failure Modes

- Bad or stale eval dataset.
- Grader bias.
- Missing trace context.
- False confidence from aggregate metrics.

## English Interview Script

I would design the eval platform as a versioned experiment system. It stores datasets and test cases, runs evaluations asynchronously, captures traces and outputs, applies automatic or human graders, and compares results across versions to catch regressions.

## TODOs

- Add example metrics for support automation.
- Add permissions and audit logging.
