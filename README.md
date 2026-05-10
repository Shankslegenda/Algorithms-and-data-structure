4-assignment
Sacenov Aldiyar
IT-2501



This project implements a directed graph using an Adjacency List. The system is designed to represent relationships between nodes (Vertices) and their connections (Edges), and then navigate those connections using two primary search algorithms.

Vertices: Represent the fundamental units or "nodes" in the graph.

Edges: Represent the links or "paths" between two vertices.

Traversals: Procedures for visiting every vertex in a specific order to search for data or analyze connectivity.

B. Class Descriptions
Vertex: A simple class holding a unique id. It serves as the data point for the graph.

Edge: Represents a directed connection between a source vertex and a destination vertex.

Graph: The core data structure. It uses an Adjacency List (a Map of lists) to store connections. This is more memory-efficient than a matrix for sparse graphs, as it only stores existing edges.

Experiment: A driver class that automates the creation of 10, 30, and 100-node graphs and uses System.nanoTime() to benchmark performance.

C. Algorithm Descriptions
1. Breadth-First Search (BFS)

Step-by-step:

Start at a source node and mark it as visited.
Add the node to a Queue.
While the queue is not empty:
Dequeue a vertex and visit all its unvisited neighbors.
Mark neighbors as visited and add them to the queue.
Use Cases: Finding the shortest path in unweighted graphs, GPS navigation, and social networking (finding "friends of friends").
Time Complexity: O(V+E)
2. Depth-First Search (DFS)
Step-by-step:
Start at a source node and mark it as visited.
Recursively (or using a Stack) visit the first unvisited neighbor.
Continue "diving" deep into the graph until a node with no unvisited neighbors is reached.
Backtrack to the previous node and repeat.
Use Cases: Pathfinding in mazes, cycle detection in circuits, and topological sorting (scheduling tasks).
Time Complexity: O(V+E)

D. Data Processing & Analysis
Experimental Results
<img width="524" height="315" alt="image" src="https://github.com/user-attachments/assets/29aaa1fe-98b3-44aa-9fc2-6ecea7345ae9" />
Analysis Questions

How does graph size affect BFS and DFS performance?
As the number of vertices and edges increases, the execution time grows linearly. A 100-node graph takes significantly longer than a 10-node graph because more objects must be stored and more connections must be checked.

Which traversal is faster in your experiments?
(Answer based on your output) Usually, DFS can be slightly faster in small graphs due to less overhead than the Queue management in BFS, but the difference is often negligible at this scale.

Do results match the expected complexity O(V+E)?
Yes. The execution times generally scale in proportion to the increase in the number of nodes and edges, confirming linear time complexity.

How does graph structure affect traversal order?
BFS explores the graph in "waves" (layer-by-layer), while DFS explores "paths" (branch-by-branch). In a line-shaped graph, they look similar; in a wide, bushy graph, the order is completely different.

When is BFS preferred over DFS?
BFS is preferred when you need the shortest path from a starting point, as it explores all nodes at distance 1 before moving to distance 2.

What are the limitations of DFS?
DFS can get "lost" down a very deep or infinite branch. In Java, a very deep recursion can also cause a StackOverflowError.

E. Reflection
In this assignment,I learned the practical trade-offs between BFS and DFS. While they have the same theoretical Big-O complexity, their behavior in memory is quite different—BFS requiring a Queue and DFS relying on the call stack.

One challenge that  I had was ensuring the adjacency list was  initialized for all vertices before adding edges, otherwise, a NullPointerException would occur. Overcoming this taught me the importance of robust constructor design in data structures.

