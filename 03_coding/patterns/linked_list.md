# Linked List

## 中文理解

链表题重点是指针关系和边界。能用 dummy node 就用，减少头节点特殊情况。设计题常和 hashmap 搭配。

## English Interview Script

For linked list problems, I use a dummy node when head changes are possible. I carefully track previous, current, and next pointers, and I state the invariant before changing links.

## Common Mistakes

- Losing the next pointer
- Forgetting head/tail updates
- Not removing old links in cache design
- Mishandling one-node or empty-list cases

## Template / Mental Model

- Use dummy node for mutations.
- Save `next` before rewiring.
- Update both directions for doubly linked lists.
- Test empty, one-node, and two-node cases.
