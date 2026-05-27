# Observability

## 中文理解

AI workflow 的 observability 不只是 logs/metrics/traces，还要能看到 prompt、tool call、模型输出、grader 结果和用户/人工反馈。

## Core Concepts

- Structured logs
- Metrics
- Distributed tracing
- Prompt and response capture with privacy controls
- Tool call traces
- Eval result correlation

## Interview Talking Points

- Debugging needs step-level traces.
- Privacy and retention policies matter.
- Aggregate dashboards should link to examples.

## System Design Hooks

- Trace store
- Metrics pipeline
- Error taxonomy
- Replay tooling

## Failure Modes

- Logs miss key context
- Too much sensitive data captured
- No correlation ID across steps
- Dashboard hides tail failures

## TODOs

- Add incident debugging script.
