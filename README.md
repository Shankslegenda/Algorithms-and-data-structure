Bonus task
Dijkstra's algorithm is a greedy graph search algorithm that calculates the shortest path from a single starting node to all other reachable nodes in a weighted graph. It is widely used in digital mapping,like GPS route planning and network routing




Weight Representation: A 2D array int[][] matrix is used where matrix[u][v] stores the weight of the edge between vertex u and vertex v. A weight of 0 denotes that no direct edge exists.
Algorithm Style: Implemented using standard arrays for tracking distances and visited nodes with simple loops O(V^2) time complexity) 
---

To build the graph, I used a 2D array called an adjacency matrix, which is basically a grid where the rows and columns are the code's vertices, and the numbers inside are the weights of the lines connecting them.Before starting , the code sets up two arrays—one to keep track of the shortest distances (which start out at infinity because we don't know them yet) and a true/false one to check off vertices we've already visited.The algorithm sets the distance of the starting vertex to 0 so the code knows exactly where to kick things off.The code runs a loop that looks at all the unvisited vertices and picks the one that currently has the smallest distance number.Once it picks that closest vertex, it marks it as "visited" so it doesn't waste time checking it again.Then, it looks at all the neighbors of that vertex, and if walking through the current vertex makes a shorter path than the one we found before, it updates that neighbor's distance score.

Example Output

<img width="423" height="214" alt="Снимок экрана 2026-05-21 в 12 39 15" src="https://github.com/user-attachments/assets/807d9a5c-a725-49c2-85f3-0990af36a201" />
