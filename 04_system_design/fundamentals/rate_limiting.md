# Rate Limiting

## 中文理解

限流保护系统，也可以保护工具、用户、租户和成本。重点是限谁、按什么维度限、在哪里限、超限后如何响应。

## English Interview Script

I define the limit dimension first: user, IP, API key, tenant, or tool. Then I choose an algorithm such as token bucket or sliding window and decide whether enforcement is local, centralized, or hybrid.

## Algorithms

- Fixed window
- Sliding window log
- Sliding window counter
- Token bucket
- Leaky bucket

## TODOs

- Add Redis-based distributed limiter details.
