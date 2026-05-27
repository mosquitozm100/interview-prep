# Binary Search

## 中文理解

二分不是只找数字，也可以在答案空间里找最小可行值或最大可行值。关键是定义单调性和边界。

## English Interview Script

I use binary search when the search space has a monotonic property. I define a predicate that tells whether a candidate is feasible, then narrow the range while preserving the invariant.

## Common Mistakes

- Wrong loop condition
- Infinite loop due to midpoint update
- Predicate not actually monotonic
- Off-by-one on final answer

## Template / Mental Model

- For exact search: maintain `left <= right`.
- For lower bound: maintain first feasible candidate.
- Always state what `left` and `right` mean.
