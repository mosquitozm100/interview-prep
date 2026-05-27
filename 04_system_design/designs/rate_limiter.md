# Rate Limiter

## 中文理解

限流的本质是保护系统和资源，避免某个用户、租户、IP 或工具调用把系统打爆。AI backend 场景里还可以限制成本、风险和工具滥用。

## Requirements

- Limit requests by user/API key/IP/tenant.
- Support configurable limits.
- Return clear rejection response.
- Work across multiple service instances.

## APIs

- `allow_request(subject, action) -> allowed | rejected`
- `update_limit(subject, rule)`

## Data Model

- Rule: subject type, limit, window, burst
- Counter/token state: subject, window, remaining tokens, updated time

## High-Level Design

- API gateway or service middleware calls limiter.
- Limiter uses Redis or similar fast shared store.
- Config service stores rules.
- Metrics track allowed, rejected, and latency.

## Deep Dives

- Token bucket for burst tolerance.
- Sliding window for smoother fairness.
- Local cache plus central store for performance.

## Bottlenecks

- Hot keys for large tenants.
- Redis latency or availability.
- Clock skew if using time windows.

## Tradeoffs / 取舍

- Centralized limiter is consistent but adds latency.
- Local limiter is faster but less globally accurate.

## Failure Modes

- Redis unavailable.
- Config stale.
- Over-limiting legitimate traffic.

## English Interview Script

I would first define the limiting dimensions and correctness requirements. For a distributed backend, I would use a centralized fast store like Redis with token bucket or sliding window counters, add local caching for config, and expose metrics for rejected traffic and limiter latency.

## TODOs

- Add exact Redis commands or Lua script approach.
- Add AI tool governance angle.
