# Tree

## 中文理解

树题通常是在递归返回值里编码信息。先想清楚每个节点需要从子树拿到什么，以及要向父节点返回什么。

## English Interview Script

For tree problems, I define what each recursive call returns. Then I combine left and right subtree results at the current node and update any global or parent-facing state.

## Common Mistakes

- Mixing global answer with return value
- Forgetting null base case
- Returning the wrong value to parent
- Not handling skewed trees

## Template / Mental Model

1. Define base case.
2. Define return value.
3. Combine children.
4. Update answer.
5. Return parent-facing result.
