# Interval

## 中文理解

区间题通常先排序，然后决定是合并、扫描线、贪心选结束时间，还是用堆处理并发。

## English Interview Script

For interval problems, I usually sort by start or end time, then maintain the active interval state. The exact strategy depends on whether we are merging, counting overlaps, or selecting non-overlapping intervals.

## Common Mistakes

- Sorting by the wrong key
- Overlap condition off by one
- Confusing closed and half-open intervals
- Forgetting to flush the last interval

## Template / Mental Model

- Define interval semantics.
- Sort by the useful key.
- Maintain current merged interval or active set.
- Update answer on each boundary.
