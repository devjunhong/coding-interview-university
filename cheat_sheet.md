## Table of Contents
- [BFS](#bfs)

## BFS

```Python
	def bfs(graph, start):
		visited, queue = set(), [start]
		while queue:
			vertex = queue.pop(0)
			if vertex not in visited:
				visited.add(vertex)
				queue.extend(graph[vertex] - visited)
		return visited
```