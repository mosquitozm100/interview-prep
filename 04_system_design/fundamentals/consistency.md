# Consistency

## 中文理解

一致性要和业务后果绑定。不是所有地方都需要强一致；库存、权限、扣费更敏感，计数、日志、分析可以更异步。

## English Interview Script

I choose consistency based on the consequence of stale data. For critical mutations I prefer transactional or strongly consistent paths; for analytics and logs I can accept eventual consistency.

## Tradeoffs

- Strong consistency: simpler correctness, higher latency or lower availability
- Eventual consistency: better scalability, more complex reconciliation

## TODOs

- Add examples for booking and tool permission checks.
