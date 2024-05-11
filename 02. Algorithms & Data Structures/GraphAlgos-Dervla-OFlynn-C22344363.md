#Algo 
<h1 style="text-align:center;"> <mark style="text-align:center; background: #69E7E4;">Algorithms and Data Structures Graph Assignment </mark> </h1>

 <h2 style="text-align:center;"><mark style="background: #69E7E4;">Dervla O'Flynn – C22344363 </mark> </h2>

1. Introduction and Explanation.
2. Adjacency List Diagram .
3. Step-by-step construction of the MST using Prim’s Algorithm. 
4. Step-by-step construction of the SST using Dijkstra’s Algorithm. 
5. Step-by-step construction of the MST for Kruskal and the union-find. Partition and set representations for Kruskal at each step.  
6. Diagram showing the MST superimposed on the graph. 
7. Diagram showing the SST superimposed on the graph. 
8. Screenshots of the executed programs. 
9. Reflection. 

 <h3 style="text-align:center;"><mark style="background: #69E7E4;">1. INTRODUCTION AND EXPLANATION</mark> </h3>

Programming was completed in cooperation with:
- Ruán Murgatroyd - C22400846 
- James Lawlor C22388703.

This is a report on the Java Program implementation of graph algorithms. There are two files: **PrimDijkstraBFDF.java** and **kruskal.java**. The graph is represented in an adjacency list in the file **wGraph.txt** that the programs read and construct the graph from. The list's first line contains how many nodes and how many vertices are in the graph. Each subsequent line has three values: the starting vertex, the end vertex and the weight of the edge.

<mark style="background: #69E7E4;">Depth First:</mark>
The Depth First Search is an algorithm that searches every node in a data structure, starting from a given root node. In this program it is located in the file **PrimDijkstraBFDF.java**. It initialises the ``visited[]`` array to 0 and begins searching from it's given root vertex. 
Using recursion it searches the graph as far as possible until it has to backtrack. It keeps calling itself until every vertex has been visited and outputs each vertex it visits as it goes.

<mark style="background: #69E7E4;">Breadth First:</mark>
The Breath First Search is an algorithm that searches every node in a data structure, starting from a given root node. In this program it is located in the file **PrimDijkstraBFDF.java**. It initialises the ``visited[]`` array to 0 and begins searching from it's given root vertex. It creates a queue and adds the starting vertex to the queue. 
While the queue isn't empty, and the next vertex hasn't been visited, the selected node is added to the ``visited[]`` array and outputs this. The next node is added to the queue, then visited until all have been.

<mark style="background: #69E7E4;">Prim's Algorithm:</mark>
Prim's algorithm is a greedy algorithm that finds a minimum spanning tree for a connected weighted undirected graph. In this program it is located in the file **PrimDijkstraBFDF.java**. It finds a subset of the edges that form a tree which includes every vertex, where the total weight of all the edges in the tree is as small as possible. This was implemented using a heap and linked lists.

<mark style="background: #69E7E4;">Dijkstra's Algorithm:</mark>
Dijkstra's Algorithms is an algorithm that finds the shortest path between two vertices in a graph. It requires a start vertex and a destination vertex. It chooses the shortest vertex each time until it has reached the destination and seeks to find the shortest path. This was implemented using a heap and linked lists.

<mark style="background: #69E7E4;">Kruskal's Algorithm:</mark>
Kruskal's Algorithm is similar to Prim's Algorithm but it does not construct the MST from a root node. Instead, it chooses the shortest edge not currently in the MST that does not form a cycle and continues until there are no unconnected vertices left over. It contains Sets of all the nodes connected to each other at each given iteration. This was implemented using a heap.

 <h3 style="text-align:center;"><mark style="background: #69E7E4;">2. ADJACENCY LIST DIAGRAM</mark> </h3>

![|350](https://i.imgur.com/VyBs8SL.png)


<h3 style="text-align:center;"><mark style="background: #69E7E4;"> 3.  STEP-BY-STEP RECONSTRUCTION OF THE MST USING PRIM'S ALGORITHM:</mark></h3>


1. Vertex L is connected to 5 edges. The lowest weight (1) is selected and now L and M are connected. 
Heap contents: [0, 6, 10, 7, 5, 0, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 0, 0, 0, 0, 12, 12, 12, 0, 0, 13, 0, 0, 12]
Distance contents: [-2147483648, 2147483647, 2147483647, 2147483647, 2147483647, 4, 2, 5, 2147483647, 2147483647, 2, 2147483647, 0, -1]
![|300](https://i.imgur.com/0XvxhsF.png)

2. Vertex L is connected to Vertex F. The weight of the edge is 2. The total weight is 3:
Heap contents: [0, 4, 10, 7, 5, 1, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 6, 0, 0, 6, 6, 12, 12, 0, 0, 13, 0, 0, 12]
Distance contents: [-2147483648, 2, 2147483647, 2147483647, 1, 2, -2, 5, 2147483647, 2147483647, 2, 2147483647, 0, -1]   
![|300](https://i.imgur.com/mYlKvIa.png)


3. Vertex F is connected to Vertex D. The weight of the edge is 1. The total weight is 4:
Heap contents: [0, 4, 10, 7, 5, 1, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 6, 0, 0, 6, 6, 12, 12, 0, 0, 13, 0, 0, 12]
Distance contents: [-2147483648, 2, 2147483647, 2147483647, 1, 2, -2, 5, 2147483647, 2147483647, 2, 2147483647, 0, -1]
![|300](https://i.imgur.com/wmzt3nD.png)

4. Vertex F is connected to Vertex A. The weight of the edge is 2. The total weight is 6:
Heap contents: [0, 2, 10, 7, 5, 0, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 6, 1, 0, 6, 6, 12, 12, 0, 0, 13, 0, 0, 12]
Distance contents: [-2147483648, -2, 1, 2147483647, -1, 2, -2, 5, 2147483647, 2147483647, 2, 2147483647, 0, -1]
![|300](https://i.imgur.com/kXZmJW9.png)

5. Vertex A is connected to Vertex B. The weight of the edge is 1. The total weight is 7:
Heap contents: [0, 3, 5, 7, 10, 0, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 6, 1, 2, 6, 6, 12, 12, 0, 0, 13, 0, 0, 12]
Distance contents: [-2147483648, -2, -1, 1, -1, 2, -2, 5, 2147483647, 2147483647, 2, 2147483647, 0, -1]
![|300](https://i.imgur.com/qU3ldsE.png)

6. Vertex B is connected to Vertex C. The weight of the edge is 1. The total weight is 8:
Heap contents: [0, 10, 5, 7, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 6, 1, 2, 6, 6, 12, 12, 0, 0, 13, 0, 0, 12]
Distance contents: [-2147483648, -2, -1, -1, -1, 2, -2, 5, 2147483647, 2147483647, 2, 2147483647, 0, -1]
![|300](https://i.imgur.com/Sj7HFrE.png)

7. Vertex M is connected to Vertex J. The weight of the edge is 2. The total weight is 10:
Heap contents: [0, 11, 7, 5, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 6, 1, 2, 6, 6, 12, 10, 0, 0, 13, 10, 0, 12]
Distance contents: [-2147483648, -2, -1, -1, -1, 2, -2, 1, 2147483647, 2147483647, -2, 1, 0, -1]
![|300](https://i.imgur.com/nUD6cNQ.png)

8. Vertex J is connected to Vertex K. The weight of the edge is 1. The total weight is 11:
Heap contents: [0, 7, 5, 9, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 6, 1, 2, 6, 6, 12, 10, 0, 11, 13, 10, 0, 12]
Distance contents: [-2147483648, -2, -1, -1, -1, 2, -2, 1, 2147483647, 1, -2, -1, 0, -1]
![|300](https://i.imgur.com/d4gP5RS.png)

9. Vertex J is connected to Vertex G. The weight of the edge is 1. The total weight is 12.
Heap contents: [0, 9, 5, 8, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 6, 1, 2, 6, 7, 12, 10, 7, 11, 13, 10, 0, 12]
Distance contents: [-2147483648, -2, -1, -1, -1, 1, -2, -1, 3, 1, -2, -1, 0, -1]
![|300](https://i.imgur.com/mTWahsj.png)


10. Vertex K is connected to Vertex I. The weight of the edge is 1. The total weight is 13:
Heap contents: [0, 5, 8, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 6, 1, 2, 6, 7, 12, 10, 9, 11, 13, 10, 0, 12]
Distance contents: [-2147483648, -2, -1, -1, -1, 1, -2, -1, 2, -1, -2, -1, 0, -1]
![|300](https://i.imgur.com/0qSLsAi.png)

11. Vertex G is connected to Vertex E. The weight of the edge is 1. The total weight is 14.
Heap contents: [0, 8, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 6, 1, 2, 6, 7, 12, 10, 9, 11, 13, 10, 0, 12]
Distance contents: [-2147483648, -2, -1, -1, -1, -1, -2, -1, 2, -1, -2, -1, 0, -1]
![|300](https://i.imgur.com/gGK1oY0.png)

12. Vertex I is connected to Vertex H. The weight of the edge is 2. The total weight is 16.
Heap contents: [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 6, 1, 2, 6, 7, 12, 10, 9, 11, 13, 10, 0, 12]
Distance contents: [-2147483648, -2, -1, -1, -1, -1, -2, -1, -2, -1, -2, -1, 0, -1]
![|300](https://i.imgur.com/wTLvYaT.png)


<h3 style="text-align:center;"><mark style="background: #69E7E4;"> 4. STEP-BY-STEP RECONSTRUCTION OF THE MST USING DIJKSTRA'S ALGORITHM: </mark></h3>

![](https://i.imgur.com/LS5ysep.png)


1. L to A:  
Weight: 4
Path: L -> F -> A
Heap contents: [0, 5, 9, 7, 2, 0, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 6, 4, 0, 6, 12, 12, 10, 0, 11, 12, 10, 0, 12]
Distance contents: [-2147483648, 4, 5, 2147483647, 3, 4, 2, 4, 2147483647, 5, 3, 4, 0, 1]
![|300](https://i.imgur.com/pqydrPa.png)

2. L to B:
Weight: 5
Path: L -> F -> A -> B
Heap contents: [0, 3, 8, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 6, 4, 2, 6, 12, 12, 10, 7, 11, 12, 10, 0, 12]
Distance contents: [-2147483648, 4, 5, 6, 3, 4, 2, 4, 7, 5, 3, 4, 0, 1]
![|300](https://i.imgur.com/VHLr3ep.png)

3. L to C
Weight: 6
Path: L -> F -> A -> B -> C
Heap contents: [0, 8, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 6, 4, 2, 6, 12, 12, 10, 7, 11, 12, 10, 0, 12]
Distance contents: [-2147483648, 4, 5, 6, 3, 4, 2, 4, 7, 5, 3, 4, 0, 1]
![|300](https://i.imgur.com/z8PBNoD.png)

4. L to D
Weight: 3
Path: L -> F -> D
Heap contents: [0, 11, 1, 7, 5, 2, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 6, 4, 0, 6, 12, 12, 10, 0, 0, 12, 10, 0, 12]
Distance contents: [-2147483648, 4, 5, 2147483647, 3, 4, 2, 4, 2147483647, 2147483647, 3, 4, 0, 1]
![|300](https://i.imgur.com/yYE6Wrh.png)

5. L to E
Weight: 4
Path: L -> F -> E
Heap contents: [0, 7, 9, 2, 3, 0, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 6, 4, 5, 6, 12, 12, 10, 0, 11, 12, 10, 0, 12]
Distance contents: [-2147483648, 4, 5, 8, 3, 4, 2, 4, 2147483647, 5, 3, 4, 0, 1]
![|300](https://i.imgur.com/bLh50mu.png)

6. L to F
Weight: 2
Path: L -> F
Heap contents: [0, 10, 4, 7, 5, 1, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 6, 0, 0, 6, 12, 12, 12, 0, 0, 12, 0, 0, 12]
Distance contents: [-2147483648, 4, 2147483647, 2147483647, 3, 4, 2, 5, 2147483647, 2147483647, 3, 2147483647, 0, 1]
![|300](https://i.imgur.com/OOiI7Gq.png)


7. L to G
Weight: 4
Path: L -> M -> J -> G
Heap contents: [0, 9, 8, 2, 3, 0, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 6, 4, 5, 6, 12, 12, 10, 7, 11, 12, 10, 0, 12]
Distance contents: [-2147483648, 4, 5, 8, 3, 4, 2, 4, 7, 5, 3, 4, 0, 1]
![|300](https://i.imgur.com/vh2CdS5.png)

8. L to H
Weight: 7
Path: L -> M -> J -> K -> I -> H
Heap contents: [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 6, 4, 2, 6, 12, 12, 10, 7, 11, 12, 10, 0, 12]
Distance contents: [-2147483648, 4, 5, 6, 3, 4, 2, 4, 7, 5, 3, 4, 0, 1]
![|300](https://i.imgur.com/JQ8i3Xh.png)

9. L to I
Weight: 5
Path: L -> M -> J -> K -> I
Heap contents: [0, 2, 8, 3, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 6, 4, 5, 6, 12, 12, 10, 7, 11, 12, 10, 0, 12]
Distance contents: [-2147483648, 4, 5, 8, 3, 4, 2, 4, 7, 5, 3, 4, 0, 1]
![|300](https://i.imgur.com/JCVMVep.png)

10. L to J
Weight: 3
Path: L -> M -> J
Heap contents: [0, 4, 1, 7, 5, 11, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 6, 0, 0, 6, 12, 12, 10, 0, 0, 12, 10, 0, 12]
Distance contents: [-2147483648, 4, 2147483647, 2147483647, 3, 4, 2, 4, 2147483647, 2147483647, 3, 4, 0, 1]
![|300](https://i.imgur.com/X9Zj5wP.png)

11. L to K
Weight: 4
Path: L -> M -> J -> K 
Heap contents: [0, 1, 5, 7, 2, 9, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 6, 4, 0, 6, 12, 12, 10, 0, 11, 12, 10, 0, 12]
Distance contents: [-2147483648, 4, 5, 2147483647, 3, 4, 2, 4, 2147483647, 5, 3, 4, 0, 1]
![|300](https://i.imgur.com/0AqUzDA.png)

12. L to M
Weight: 1
Path: L -> M
Heap contents: [0, 6, 10, 7, 5, 0, 0, 0, 0, 0, 0, 0, 0, 0]
Parent contents: [0, 0, 0, 0, 0, 12, 12, 12, 0, 0, 12, 0, 0, 12]
Distance contents: [-2147483648, 2147483647, 2147483647, 2147483647, 2147483647, 4, 2, 5, 2147483647, 2147483647, 3, 2147483647, 0, 1]
![|300](https://i.imgur.com/cPAmqiy.png)


<h3 style="text-align:center;"><mark style="background: #69E7E4;"> 5.  STEP-BY-STEP RECONSTRUCTION OF THE MST USING KRUSKAL'S ALGORITHM: </mark></h3>
The edges are read from the graph and the initial sets are constructed

1. Starting at A, the tree travels to B. The weight of the edge is 1. The total weight is 1.
Edge A -- 1 -- B
Set: |A B |,
Set: |C |,
Set: |D |,
Set: |E |,
Set: |F |,
Set: |G |,
Set: |H |, 
Set: |I |,
Set: |J |,
Set: |K |,
Set: |L |,
Set: |M |,
Tree : A-->A B-->A C-->C D-->D E-->E F-->F G-->G H-->H I-->I J-->J K-->K L-->L M-->M
![|300](https://i.imgur.com/XT13fmb.png)

2.  From B, the tree travels to C. The weight of the edge is 1. The total weight is 2.
Edge B -- 1 -- C
Set: |A B C |,
Set: |D |,
Set: |E |,
Set: |F |,
Set: |G |,
Set: |H |,
Set: |I |,
Set: |J |, 
Set: |K |,
Set: |L |,
Set: |M |,
Tree : A-->A B-->A C-->A D-->D E-->E F-->F G-->G H-->H I-->I J-->J K-->K L-->L M-->M
![|300](https://i.imgur.com/uAw8ZlY.png)


3. Choosing the next lowest weight, the Graph travels from D to F. The weight of the edge is 1. The total weight is 3.
Edge D -- 1 -- F
Set: |A B C |,
Set: |D F |,
Set: |E |,
Set: |G |,
Set: |H |,
Set: |I |,
Set: |J |,
Set: |K |,
Set: |L |,
Set: |M |,
Tree : A-->A B-->A C-->A D-->D E-->E F-->D G-->G H-->H I-->I J-->J K-->K L-->L M-->M
![|300](https://i.imgur.com/qBxKFy2.png)

4. Choosing the next lowest weight, the graph travels from I to K. The weight of the edge is 1. The total weight is 4.
Edge I -- 1 -- K
Set: |A B C |,
Set: |D F |,
Set: |E |,
Set: |G |,
Set: |H |,
Set: |I K |,
Set: |J |,
Set: |L |,
Set: |M |,
Tree : A-->A B-->A C-->A D-->D E-->E F-->D G-->G H-->H I-->I J-->J K-->I L-->L M-->M  
![|300](https://i.imgur.com/2yOCWXW.png)

5. The tree then travels from J to K. The weight of the edge is 1. The total weight is 5.
Set: |A B C |,
Set: |D F |,
Set: |E |,
Set: |G |,
Set: |H |,
Set: |I J K |,
Set: |L |,
Set: |M |,
Tree : A-->A B-->A C-->A D-->D E-->E F-->D G-->G H-->H I-->J J-->J K-->I L-->L M-->M
![|300](https://i.imgur.com/FMySOPo.png)

6. E is then joined to G. The weight of the edge is 1. The total weight is 6.
Edge E -- 1 -- G
Set: |A B C |,
Set: |D F |,
Set: |E G |,
Set: |H |,
Set: |I J K |,
Set: |L |,
Set: |M |,
Tree : A-->A B-->A C-->A D-->D E-->E F-->D G-->E H-->H I-->J J-->J K-->I L-->L M-->M
![|300](https://i.imgur.com/Doo4ioJ.png)


7. L is joined to M. The weight of the edge is 1. The total weight is 7. 
Edge L -- 1 -- M
Set: |A B C |,
Set: |D F |,
Set: |E G |,
Set: |H |,
Set: |I J K |,
Set: |L M |,
Tree : A-->A B-->A C-->A D-->D E-->E F-->D G-->E H-->H I-->J J-->J K-->I L-->L M-->L
![|300](https://i.imgur.com/FE35078.png)


8. G is joined to J. The weight of the edge is 1. The total weight is 8.
Edge G -- 1 -- J
Set: |A B C |,
Set: |D F |,
Set: |E G I J K |,
Set: |H |,
Set: |L M |,
Tree : A-->A B-->A C-->A D-->D E-->E F-->D G-->E H-->H I-->J J-->E K-->I L-->L M-->L
![|300](https://i.imgur.com/WYMmVMY.png)

9. D is joined to E. The weight is of the edge is 2. The total weight is 10. 
Set: |A B C |,
Set: |D E F G I J K |,
Set: |H |,
Set: |L M |,
Tree : A-->A B-->A C-->A D-->D E-->D F-->D G-->E H-->H I-->J J-->E K-->I L-->L M-->L
![|300](https://i.imgur.com/GgbpIhc.png)

10. H is joined to I. The weight of the edge is 2. The total weight is 12.
Edge H -- 2 -- I
Set: |A B C |,
Set: |D E F G H I J K |,
Set: |L M |, 
Tree : A-->A B-->A C-->A D-->H E-->D F-->D G-->E H-->H I-->J J-->E K-->I L-->L M-->L
![|300](https://i.imgur.com/GvDlcZk.png)

11. J is joined to M. The weight of the edge is 2. The total weight is 14.
Set: |A B C |,
Set: |D E F G H I J K L M |,
Tree : A-->A B-->A C-->A D-->H E-->D F-->D G-->E H-->H I-->J J-->E K-->I L-->H M-->L
![|300](https://i.imgur.com/4bZDFpv.png)


12. A is joined to F. The weight of the edge is 2. The total weight is 16
Edge A -- 2 -- F
Set: |A B C D E F G H I J K L M |,
Tree : A-->A B-->A C-->A D-->H E-->D F-->D G-->E H-->A I-->J J-->E K-->I L-->H M-->L
![|300](https://i.imgur.com/lBPXzBr.png)


<h3 style="text-align:center;"><mark style="background: #69E7E4;">6. DIAGRAM SHOWING THE MST SUPERIMPOSED ON THE GRAPH</mark></h3>
<h5><mark style="background: #69E7E4;">MST from Prim's Algorithm (Weight = 16):</mark></h5>

![](https://i.imgur.com/wTLvYaT.png)

##### <mark style="background: #69E7E4;">MST from Kruskal's Algorithm (Weight = 16):</mark>

![](https://i.imgur.com/Rdin1sh.png)

<h3 style="text-align:center;"><mark style="background: #69E7E4;">7. DIAGRAM SHOWING DIJKSTRA'S SST SUPERIMPOSED ON THE GRAPH</mark></h3>

![|200](https://i.imgur.com/pqydrPa.png) ![|200](https://i.imgur.com/VHLr3ep.png) ![|200](https://i.imgur.com/z8PBNoD.png)

![|200](https://i.imgur.com/yYE6Wrh.png) ![|200](https://i.imgur.com/bLh50mu.png) ![|200](https://i.imgur.com/OOiI7Gq.png)

![|200](https://i.imgur.com/vh2CdS5.png) ![|200](https://i.imgur.com/JQ8i3Xh.png) ![|200](https://i.imgur.com/JCVMVep.png)

![|200](https://i.imgur.com/X9Zj5wP.png) ![|200](https://i.imgur.com/0AqUzDA.png) ![|200](https://i.imgur.com/cPAmqiy.png)

<h3 style="text-align:center;"><mark style="background: #69E7E4;">8. SCREENSHOTS OF THE EXECUTED PROGRAMS</mark></h3>
<h5> <mark style="background: #69E7E4;">Depth First Traversal/Breadth First Traversal/Prim's Algorithm/Dijkstra's Algorithm:</mark> </h5>

<mark style="background: #69E7E4;">Edge Count:</mark>
![](https://i.imgur.com/T6j3mVm.png)


<mark style="background: #69E7E4;">Adjaceny List:</mark>
![](https://i.imgur.com/wWYdqBv.png)

<mark style="background: #69E7E4;">Depth First:</mark>
![](https://i.imgur.com/BLWLzOM.png)

<mark style="background: #69E7E4;">Breadth First:</mark>
![](https://i.imgur.com/Qqy9vCo.png)

<mark style="background: #69E7E4;">Minimum Spanning Tree (MST) found using Prim's Algorithm:</mark>
![](https://i.imgur.com/z6nfscs.png)
![](https://i.imgur.com/dJX9qRQ.png)


<mark style="background: #69E7E4;">SST found using Dijkstra's Algorithm:</mark>
![](https://i.imgur.com/F7YiFXS.png)
![](https://i.imgur.com/LS5ysep.png)

##### <mark style="background: #69E7E4;">Kruskal's MST Algorithm:</mark>

![](https://i.imgur.com/CILaiVf.png)

![](https://i.imgur.com/tFUzn4y.png)

![](https://i.imgur.com/zSzBUTj.png)
![](https://i.imgur.com/edXhBGO.png)
![](https://i.imgur.com/mg8UT0F.png)

![](https://i.imgur.com/Kaon6XC.png)


<h3 style="text-align:center;"><mark style="background: #69E7E4;">9. REFLECTION:</mark></h3>
By doing this assignment, I learned about Graphs. I learned about Depth First Traversal, Breadth First Traversal, Prim's Algorithm, Dijkstra's Algorithm and Kruskal's Algorithm. I learned how they differ and their similarities. I learned how to implement these algorithms in Java and how to represent them in a human-readable format to standard output.

This was a useful assignment to get practical experience with these algorithms and their core mechanics. The step-by-step analysis of the graph was an ideal method to truly understand how these algorithms work.