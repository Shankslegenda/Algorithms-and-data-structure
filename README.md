Bonus task
Dijkstra's algorithm is a greedy graph search algorithm that calculates the shortest path from a single starting node to all other reachable nodes in a weighted graph. It is widely used in digital mapping,like GPS route planning and network routing




Weight Representation: A 2D array int[][] matrix is used where matrix[u][v] stores the weight of the edge between vertex u and vertex v. A weight of 0 denotes that no direct edge exists.
Algorithm Style: Implemented using standard arrays for tracking distances and visited nodes with simple loops O(V^2) time complexity) 
---

To build the graph, I used a 2D array called an adjacency matrix, which is basically a grid where the rows and columns are the code's vertices, and the numbers inside are the weights of the lines connecting them.Before starting , the code sets up two arrays—one to keep track of the shortest distances (which start out at infinity because we don't know them yet) and a true/false one to check off vertices we've already visited.The algorithm sets the distance of the starting vertex to 0 so the code knows exactly where to kick things off.The code runs a loop that looks at all the unvisited vertices and picks the one that currently has the smallest distance number.Once it picks that closest vertex, it marks it as "visited" so it doesn't waste time checking it again.Then, it looks at all the neighbors of that vertex, and if walking through the current vertex makes a shorter path than the one we found before, it updates that neighbor's distance score.

Example Output

Testing Graph Size: 10
0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 
--- Dijkstra Shortest Paths from Vertex 0 ---
Vertex     Distance       
0          0              
1          2              
2          5              
3          9              
4          14             
5          20             
6          27             
7          35             
8          44             
9          54             

Testing Graph Size: 30

--- Dijkstra Shortest Paths from Vertex 0 ---
Vertex     Distance       
0          0              
1          2              
2          5              
3          9              
4          14             
5          20             
6          27             
7          35             
8          44             
9          54             
10         65             
11         77             
12         90             
13         104            
14         119            
15         135            
16         152            
17         170            
18         189            
19         209            
20         230            
21         252            
22         275            
23         299            
24         324            
25         350            
26         377            
27         405            
28         434            
29         464            





--- FINAL PERFORMANCE RESULTS ---
Size  10 | BFS:   262125 ns | DFS:   105084 ns | Dijkstra: 13487625 ns
Size  30 | BFS:    46667 ns | DFS:    29208 ns | Dijkstra:  3591875 ns
Size 100 | BFS:    91333 ns | DFS:    54542 ns | Dijkstra:  8001208 ns
