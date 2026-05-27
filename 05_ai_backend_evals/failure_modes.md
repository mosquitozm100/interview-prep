# AI Backend Failure Modes

## 中文理解

AI backend 的失败不一定是服务挂了，也可能是质量下降、工具误用、不可解释、评估失真或人工升级失败。

## Core Concepts

- Model quality regression
- Tool call failure
- Permission failure
- Bad eval signal
- Missing observability
- Human review bottleneck

## Interview Talking Points

- Separate infrastructure failures from quality failures.
- Design fallback paths before launch.
- Make failures visible through traces and evals.

## System Design Hooks

- Circuit breakers
- Guardrails
- Retry policies
- Escalation queues
- Regression dashboards

## Failure Modes

- Silent quality regression
- Hallucinated action
- Infinite workflow loop
- Incorrect escalation decision
- Overloaded human review queue

## TODOs

- Add mitigation table.
