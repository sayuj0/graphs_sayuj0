# graphs-sayuj0

A Python library that implements classic graph algorithms.  
This package was built for a software packaging assignment and includes:

- **Dijkstra’s shortest path algorithm** (for weighted graphs)
- **BFS shortest path algorithm** (for unweighted graphs)

---

## Installation

Install the latest package:

```
pip install graphs-sayuj0
```

## Dijkstra's Shortest Path Algorithm

Dijkstra’s Shortest Path Algorithm is a classic greedy algorithm used to find the shortest path from a single source node to all other nodes in a weighted graph with non-negative edge weights. It works by maintaining a set of nodes whose shortest distance from the source is already known, then repeatedly selecting the node with the smallest tentative distance, updating the distances of its neighbors, and marking it as processed. This process continues until all reachable nodes have their shortest distances finalized. Essentially, it builds the shortest path tree step by step, ensuring that once a node’s shortest distance is determined, it is never updated again

## Breadth-First Search Algorithm

BFS is a fundamental graph traversal algorithm that explores a graph level by level, starting from a source node. It uses a queue to visit all immediate neighbors of the source before moving on to their neighbors, ensuring the closest nodes are always processed first. In unweighted graphs, BFS naturally finds the shortest path from the source to all other reachable nodes because it visits nodes in order of increasing distance. Unlike Dijkstra’s (which handles weighted graphs), BFS is simpler and more efficient when edge weights are all equal (or absent).

## Usage

Prepare a text file describing your graph:
- The first line is a header (ignored).
- Each following line contains: source destination weight

Example (graph.txt):
```
# s d w
0 1 4
0 2 1
2 1 2
2 3 5
1 3 1
```

Run the program:
```
python test.py graph.txt
```

Output:
```
Shortest distances from 0:
{0: 0, 1: 3, 2: 1, 3: 4}
spf to 0: [0]
spf to 1: [0, 2, 1]
spf to 2: [0, 2]
spf to 3: [0, 2, 1, 3]
```

## Development
- main branch is protected
- dev branch is used for active development

## Links
- PyPi: https://pypi.org/project/graphs-sayuj0/
- GitHub: 
