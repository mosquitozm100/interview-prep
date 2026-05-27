# Sliding Window

## 中文理解

滑动窗口的核心是维护一个连续区间和一个清楚的不变量。不要只记模板，要先说清楚窗口什么时候合法，什么时候需要收缩。

## English Interview Script

I use a sliding window when the answer depends on a contiguous range. I maintain counts or state for the current window, expand the right boundary, and shrink the left boundary while the window satisfies or violates the condition depending on the problem.

## Common Mistakes

- Shrinking too early or too late
- Confusing number of matched characters with number of matched unique requirements
- Forgetting to update the answer before moving the left pointer

## Template / Mental Model

1. Define window state.
2. Expand right.
3. Update state.
4. While invariant allows, shrink left.
5. Record best answer at the correct moment.
