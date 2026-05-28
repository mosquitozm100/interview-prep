# Design Fundamentals

## Requirements Clarification

- Define users, core use cases, and success criteria.
- Separate functional and non-functional requirements.

## API Design

- Start from main user flows.
- Keep APIs simple and idempotent where possible.

## Data Model

- Identify core entities and relationships.
- State which fields are required for correctness.

## Capacity Estimation

- Estimate reads, writes, storage, and peak traffic.
- Use estimates to find bottlenecks, not to chase precision.

## Caching

- Use for read-heavy or expensive data.
- Define cache key, TTL, invalidation, and fallback.

## Queues And Async Processing

- Use queues for fanout, retries, decoupling, and smoothing spikes.
- Discuss idempotency and dead-letter handling.

## Consistency

- Tie consistency to business risk.
- Use stronger consistency for inventory, permissions, and payment-like flows.

## Rate Limiting

- Define limit dimension: user, tenant, IP, API key, or tool.
- Choose fixed window, sliding window, token bucket, or hybrid.

## Realtime Communication

- Separate connection management from durable storage.
- Discuss ordering, offline recovery, and backpressure.

## Observability

- Include logs, metrics, traces, dashboards, alerts, and debugging flows.
- For AI systems, include prompts, model outputs, tool calls, and eval results with privacy controls.

## Failure Handling

- Discuss retries, timeouts, circuit breakers, fallback, and manual review.

## Tradeoff Discussion

- State the tradeoff clearly.
- Explain why the chosen approach fits the requirements.
