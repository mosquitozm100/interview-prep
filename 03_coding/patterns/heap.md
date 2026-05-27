# Heap

## 中文理解

堆适合动态拿最小/最大元素，常见于 top K、k-way merge、调度、流式数据。要注意堆里放什么字段，如何处理 tie-break。

## English Interview Script

I use a heap when I repeatedly need the smallest or largest available item while the candidate set changes over time. The heap stores just enough information to advance the process efficiently.

## Common Mistakes

- Forgetting heap size constraints for top K
- Storing too little context
- Mishandling duplicate values
- Not comparing with divide-and-conquer alternatives

## Template / Mental Model

- Define priority.
- Define heap entry fields.
- Push initial candidates.
- Pop best candidate.
- Add next candidate if needed.
