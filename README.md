# Data Structures

A **data structure** is a container used to store and organize data. They are used to arrange data on a computer for efficient access and updates. We previously introduced the basic concepts and types of data structures, as well as our implementations in C++ of linear and data structures, such as a **Stack**, a **Queue**, a **Circular Queue**, a **Linked List** and a **Hash Table**. Please refer to the repo [linear_data_structures](https://github.com/alan-xavier-16/linear_data_structures) for details.

In this repo, we will implement the **Graph** data structures.

## Graph Data Structures

A graph data structure is a **collection of nodes** that have `data` and are `connected` to other nodes. Every connection or relationship between nodes is represented by an edge. In summary, a graph `(V, E)` consists of

- A collection of `vertices V`
- A collection of `edges E`, represented as `ordered pairs of vertices (u,v)`

For example, `V = {0, 1, 2, 3}` and `E = {(0,1), (0,2), (0,3), (1,2)}` can represent a graph data structure.

```C++
3--0--1
   | /
   2
```

## Graph Terminology

- `Adjacency`: vertices are **adjacent** if there is an edge connecting them. In the example above, vertices 2 and 3 are not adjacent as there is no edge between them.
- `Path`: A path is a **sequence of edges** that allows traversal from vertex A to B. For example, `0-1, 1-2 and 2-0` are paths from vertex 0 to 2.
- `Directed Graph`: A graph in which an edge (u,v) have a **direction**. The edges in such a graph are represented by arrows to show the direction of the edge.

## Graph Representation

Graphs are commonly represented in two ways:

### Adjacency Matrix

An adjacency matrix is a `2D array` of `V x V` vertices, where each row and column represent a vertex in the graph. If the value of any element in the array `a[i][j] is 1`, then there is an edge connecting vertex `i` to `j`.

| ![Adjacency Matrix](./assets/Adjacency%20Matrix.png) |
| ---------------------------------------------------- |

`Edge lookup` (checking if an edge exists between vertex A and B) is extremely fast in the adjacency matrix representation, however more space is required for every possible link between all vertices (V x V).

### Adjacency List

An adjacency list represents a graph as an `array of linked lists`. The `index` of the array represents a **vertex** and `each element` in its linked list forms an **edge** with this vertex.

| ![Adjacency List](./assets/Adjacency%20List.png) |
| ------------------------------------------------ |

An adjacency list is efficient in terms of storage because we only need to store the values for the edges.

## Graph Operations

Common graph operations are:

- Check if the element is present in the graph
- Graph Traversal
- Add elements (vertex, edges) to graph
- Finding the path from one vertex to another

## Spanning Tree and Minimum Spanning Tree

- An `undirected` graph is a graph where the edges do not have any direction.
- A `connected` graph is a graph where there is **always** a path from one vertex to any other vertex.
- A `complete` graph is an undirected graph where every pair of vertices is connected by an edge.

### Spanning tree

A spanning tree is a sub-graph of an **undirected** graph, which includes `all the vertices` with a `minimum possible number of edges`. The edges may or may not have `weights` assigned to them.

The **total number** of spanning trees with `n` vertices that can be created from a complete graph is `n^(n-2)`.

### Minimum Spanning Tree

A minimum spanning tree is a spanning tree where the `sum` of the `weight` of the edges is as `minimum` as possible.

## References

1. [Programiz Graph Data Structures](https://www.programiz.com/dsa/graph)
