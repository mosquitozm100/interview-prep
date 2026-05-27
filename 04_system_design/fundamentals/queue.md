# Queue

## 中文理解

队列用于削峰、异步处理、解耦服务。面试里要讲清楚重试、幂等、死信队列、顺序和可观测性。

## English Interview Script

I use queues when work can be processed asynchronously. I design for retries, idempotency, dead-letter handling, backpressure, and visibility into stuck jobs.

## Key Questions

- Is ordering required?
- Can the job be retried safely?
- What is the maximum acceptable delay?
- What happens when downstream is down?

## TODOs

- Add async job platform notes.
