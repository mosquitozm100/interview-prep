# Graph

## 中文理解

图题先建模：节点是什么，边是什么，权重有没有，是否有方向。之后再决定 BFS、DFS、Dijkstra、拓扑排序或并查集。

## English Interview Script

I first model the problem as nodes and edges, then choose the traversal based on what the question asks. For shortest unweighted paths I use BFS; for reachability I often use DFS/BFS; for dependencies I use topological sort.

## Common Mistakes

- Marking visited too late in BFS
- Not handling cycles
- Building neighbors too slowly
- Confusing shortest path in weighted vs. unweighted graphs

## Template / Mental Model

- Model nodes and edges.
- Pick traversal.
- Track visited state.
- Define level, distance, or component meaning.
- Analyze graph construction cost.
