# Caching

## 中文理解

缓存是为了降低延迟和后端压力，但会引入失效、一致性和热点问题。先说明 cache key、TTL、失效策略和 fallback。

## English Interview Script

I use caching for read-heavy or expensive data. I define cache keys, TTLs, invalidation strategy, and behavior on cache miss or backend failure.

## Common Patterns

- Cache-aside
- Write-through
- Write-back
- Negative caching

## TODOs

- Add cache story for URL shortener and eval result reads.
