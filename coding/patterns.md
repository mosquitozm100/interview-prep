# Coding Patterns

## Sliding Window

- When to use: contiguous subarray or substring with dynamic constraints.
- Common mistakes: unclear window invariant, wrong shrink condition.
- Representative problems: Minimum Window Substring, Longest Substring Without Repeating Characters.

## Binary Search

- When to use: sorted search space or monotonic feasibility.
- Common mistakes: off-by-one, non-monotonic predicate.
- Representative problems: Search in Rotated Sorted Array, Koko Eating Bananas.

## Tree DFS/BFS

- When to use: recursive structure, level traversal, path or subtree aggregation.
- Common mistakes: mixing return value with global answer.
- Representative problems: Binary Tree Maximum Path Sum, Level Order Traversal.

## Graph BFS/DFS

- When to use: reachability, shortest unweighted path, components.
- Common mistakes: marking visited too late, building neighbors inefficiently.
- Representative problems: Word Ladder, Number of Islands.

## Topological Sort

- When to use: dependency ordering or cycle detection in directed graphs.
- Common mistakes: wrong indegree updates, missing cycle check.
- Representative problems: Alien Dictionary, Course Schedule.

## Heap / Top K

- When to use: repeatedly need min/max, merge sorted streams, top K.
- Common mistakes: storing too little context, wrong heap size.
- Representative problems: Merge k Sorted Lists, Top K Frequent Elements.

## Linked List

- When to use: pointer manipulation, cache design, fast/slow pointers.
- Common mistakes: losing next pointer, missing dummy node.
- Representative problems: LRU Cache, Reverse Linked List.

## Dynamic Programming

- When to use: overlapping subproblems and optimal substructure.
- Common mistakes: weak state definition, wrong iteration order.
- Representative problems: Coin Change, Longest Increasing Subsequence.

## Intervals

- When to use: overlapping ranges, scheduling, merge or count active intervals.
- Common mistakes: sorting by wrong key, closed vs half-open confusion.
- Representative problems: Merge Intervals, Meeting Rooms II.

## Stack / Monotonic Stack

- When to use: nested parsing, previous/next greater element, expression evaluation.
- Common mistakes: forgetting pending operators, wrong comparison direction.
- Representative problems: Basic Calculator II, Daily Temperatures.
