# Chapter 1: Introduction to Data Structures
## Topic 1: Why Are Data Structures Needed?

### 1.1 Overview and Core Concept
In computer science, data must be stored, accessed, processed, modified, and managed efficiently. A data structure is a way of organizing and storing data so that particular operations can be performed efficiently.

Different data structures are designed to support different operations. Choosing an appropriate structure can improve an algorithm's execution time, memory usage, and maintainability.

Without a suitable data structure, a program may require excessive computation or memory as the amount of data increases. However, no single data structure is optimal for every situation. The best choice depends on the data, the operations required, and the system's performance constraints.

#### Example
Suppose a university needs to store the records of 10,000 students. Each record may contain:
- Student ID
- Name
- Age
- Department
- Examination scores

Storing every value in an unrelated variable would make the records difficult to manage. Instead, the university could organize the records using arrays, lists, hash tables, or database structures, depending on its requirements:
* **An array** may store examination scores in order.
* **A hash table** may associate student IDs with student records.
* **A tree** may represent a hierarchical organizational structure.
* **A graph** may represent connections between students or departments.

The choice of data structure affects how efficiently the information can be accessed and modified.

---

### 1.2 Key Motivations and Technical Advantages

#### A. Resource Efficiency: Time and Space Optimization
Data structures influence the time and memory required to perform operations.
* **Time complexity** describes how the computational work of an algorithm grows as the input size increases.
* **Space complexity** describes how the memory requirements of an algorithm grow as the input size increases.

For example, consider searching for a student ID in a collection:
* Searching an unsorted array requires $O(n)$ time in the worst case.
* Searching a balanced Binary Search Tree (BST) generally requires $O(\log n)$ time.
* Searching a hash table typically requires $O(1)$ time on average under suitable assumptions.

These complexities are not interchangeable guarantees. They depend on the data structure's properties, implementation, and the operation being performed.

#### B. Scalability
Scalability refers to a system's ability to handle increasing amounts of data or work while maintaining acceptable performance. Data structures help manage growing collections efficiently, but they do not automatically make an application scalable. Performance also depends on algorithms, hardware, networking, concurrency, and software architecture.

#### C. Abstraction and Reusability
Data structures allow programmers to organize data behind well-defined operations. An implementation can be reused across different applications, reducing the need to rewrite the same logic. 

For example, a stack can be used for:
* Undo operations in text editors
* Function-call management
* Expression evaluation
* Backtracking algorithms

#### D. Modeling Real-World Relationships
Real-world information often contains relationships that cannot be represented conveniently by isolated values.

| Relationship | Suitable Structure | Example |
| :--- | :--- | :--- |
| **Sequential** | Array or linked list | Examination scores |
| **Last in, first out** | Stack | Undo operations |
| **First in, first out** | Queue | Processing tasks in arrival order |
| **Hierarchical** | Tree | File systems |
| **Priority-based** | Priority queue | Job scheduling |
| **Interconnected** | Graph | Road networks |
| **Key-value association** | Hash table | Student ID lookup |

#### E. Trade-Offs Between Data Structures
* **Arrays** provide efficient indexed access but may require shifting elements during insertion or deletion.
* **Linked lists** support efficient insertion or deletion when the relevant position is already accessible, but indexed access is slow.
* **Hash tables** offer fast average-case lookup by key but do not inherently maintain sorted order.
* **Balanced search trees** support ordered traversal and efficient search, insertion, and deletion, generally in $O(\log n)$ time.

---

### 1.3 Introduction to Algorithm Analysis
Algorithm analysis helps estimate how efficiently an algorithm performs as its input grows ($n$).

#### A. Common Time Complexes
| Complexity | Name | General Meaning | Example |
| :--- | :--- | :--- | :--- |
| $O(1)$ | Constant | Work does not grow with input size | Accessing an array element by index |
| $O(\log n)$ | Logarithmic | Work grows slowly as input increases | Binary search |
| $O(n)$ | Linear | Work grows proportionally to input size | Linear search |
| $O(n \log n)$ | Linearithmic | Common in efficient sorting | Merge sort |
| $O(n^2)$ | Quadratic | Work grows with nested iterations | Simple nested-loop comparison |

#### B. Best, Average, and Worst Cases
* **Best case:** The most favorable input conditions.
* **Average case:** Expected performance under a specified input distribution.
* **Worst case:** The maximum amount of work required for inputs of a given size.

---

### 1.4 Choosing the Right Data Structure
| Requirement | Possible Choice | Reason |
| :--- | :--- | :--- |
| **Frequent access by index** | Array | Constant-time indexed access |
| **Frequent lookup by key** | Hash table | Average-case constant-time lookup |
| **Processing items in arrival order** | Queue | First-in, first-out behavior |
| **Reversing operations** | Stack | Last-in, first-out behavior |
| **Selecting highest-priority item** | Priority queue | Efficient priority-based retrieval |
| **Maintaining sorted data with updates**| Balanced search tree | Efficient ordered operations |
| **Representing arbitrary connections** | Graph | Models vertices and edges |

![image alt](https://github.com/Jrmy-y/Wahaha-Project/blob/231a2bd47004b002b1cdfbf0be82b815034ed6d2/Assets/Images/stack-vs-queue.webp)

---

## Topic 2: Data vs. Data Types vs. Data Structures

### 2.1 Definitions and Comparison
| Feature | Data | Data Type | Data Structure |
| :--- | :--- | :--- | :--- |
| **Definition** | Information represented as values or symbols | A classification defining valid values and supported operations | A way of organizing and storing data elements |
| **Main Question** | What information is represented? | What kind of value is this? | How are values organized and accessed? |
| **Purpose** | Represent information | Define how values are interpreted and used | Support efficient operations on collections or relationships |
| **Examples** | `85`, `"Hello"`, `3.14`, `true` | `int`, `float`, `bool`, `str` | Array, linked list, tree, graph, hash table |

---

### 2.2 Abstract Data Types and Implementations
An **Abstract Data Type (ADT)** defines a data type in terms of its behavior and supported operations, without requiring a particular internal implementation.

#### Example: Stack ADT
* `push(x)`: Add `x` to the top.
* `pop()`: Remove and return the top element.
* `peek()`: Return the top element without removing it.
* `isEmpty()`: Check whether the stack is empty.

---

### 2.3 Logical Organization vs. Physical Memory Layout
* **Contiguous Storage (e.g., Arrays):** Elements occupy consecutive memory locations. Provides efficient indexed access and good memory locality.
* **Linked Storage (e.g., Linked Lists):** Elements stored in nodes connected by pointers/references across non-consecutive addresses.
![image alt](https://github.com/Jrmy-y/Wahaha-Project/blob/231a2bd47004b002b1cdfbf0be82b815034ed6d2/Assets/Images/Array%20vs%20Link.png)
---

## Topic 3: Classification and Basic Operations

### 3.1 Classification of Data Structures
* **Primitive vs. Non-Primitive:** Basic programming types vs. complex grouped structures.
* **Linear vs. Non-Linear:** Sequential sequences (Arrays, Queues) vs. hierarchical/interconnected layouts (Trees, Graphs).
* **Static vs. Dynamic:** Fixed capacity vs. resizable during execution.


### 3.2 Fundamental Operations
Common operations include **Traversal**, **Searching**, **Insertion**, **Deletion**, **Updating**, **Sorting**, and **Accessing**.

---

## Topic 4: Real-Life Applications

* **4.1 Arrays and Dynamic Arrays:** Best for indexed collections and sequential numerical sets ($O(1)$ lookup).
* **4.2 Linked Lists:** Ideal for frequent insertions/deletions at accessible pointers.
* **4.3 Stacks ($LIFO$):** Used in undo/redo actions, call stacks, and expression evaluations.
* **4.4 Queues ($FIFO$):** Used in printer scheduling, server requests, and Breadth-First Search (BFS).
* **4.5 Hash Tables:** Excellent for caching, symbol tables, and key-value lookups ($O(1)$ average case).
* **4.6 Trees:** Hierarchical file systems, DOM trees, and Abstract Syntax Trees (ASTs).
![image alt](https://github.com/Jrmy-y/Wahaha-Project/blob/231a2bd47004b002b1cdfbf0be82b815034ed6d2/Assets/Images/Tree%20vs%20Graph.webp)
* **4.7 Heaps & Priority Queues:** Event-driven simulations, task queues, and Dijkstra's algorithm.
* **4.8 Graphs:** Social networks, GPS routing, and recommendation systems.

---


# Chapter 2: Algorithms
What is an algorithm? An algorithm is basically a recipe to a recipe. A list of steps that turns input into output which doesn't vary, furthermore it is the building block of every AI.


## Topic 1: Foundation of Algorithms Analysis
There are 3 ways to analyse an algorithm:
- Exact operation count
  a mathematical count or model of the computational operations an algorithm performs for a   
  particular input size and a particular input.
- Asymptotic growth
  Describes how an algorithm's operation count changes as its input size becomes very large
- Measured Execution time
  The actual time an implementation tkaes to run on a particular machine under particular 
  conditions.

  
### 1.1 Asymptotic notation
Asymptotic notation is a mathematical system for describing how an algorithm's resource requirements grow as its input size approaches infinity.
<br/>
<br/>
Asymptotic analysis allows us to compare algorithms without depending on a specific processor, programming language or machine speed.<br/>
<br/>
#### Main asymptotic notations
- Big O: Asymptotic upper bound
  This notation gives the upper bound on the eventual growth of a function.<br/>
  $T(n) = O(g(n))$<br/>where $0 \leq f(n) \leq cg(n)$ <br/> for all   $n \geq n_0$<br/>
- Big Omega: Asymptotic lower bound
  This notation gives the lower bound on the eventual growth of a function
  $T(n) = \Omega(g(n))$<br/>where $0 \leq cg(n) \leq f(n)$ <br/> for all   $n \geq n_0$<br/>
- Big Theta: Tight asymptotic bound
  This notation gives an upper and lower bound
  $T(n) = \Theta(g(n))$<br/>where $0 \leq c_1g(n) \leq f(n) \leq c_2g(n)$ <br/> for all   $n \geq n_0$<br/>
- Little o: Strict asymptotic upper bound
  Little o expresses a strictly slower growth rate
  $T(n) = o(g(n))$<br/>where $0 \leq c_1g(n) \leq f(n) \leq c_2g(n)$ <br/> for all   $n \geq n_0$<br/>
- Little omega: Strict asymptotic lower bound
  Little omega expresses strictly faster growth rate
   $T(n) = \omega(g(n))$<br/>where $f(n)$ eventually grows faster than every constant multiple 
   $g(n)$
<br/>


| Complexity | Common Name |
|:----------:|:-----------:|
| $O(1)$ | Constant |
| $O(\log n)$ | Logarithmic |
| $O(n)$ | Linear |
| $O(n\log n)$ | Linearithmic|
| $O(n^2)$ | Quadratic |
| $O(n^3)$ | Cubic |
| $O(2^n)$ | Exponential |
| $O(n!)$ | Factorial|

<br/>

#### Common mistakes
- Do not confuse Big O with exact running time
- Do not claim that Big O always means worst case
- Do not compare algorithms solely by asymptotic notations when inputs are small or implementation constants are significant.<br/><br/>


### 1.2 Recurrence Relations
A recurrence relation expresses a function in terms of its values on smaller inputs. 
In algorithm analysis, we use this to analyse recursive algorithms.<br/>
Why?<br/>
Because recursive algorithms have looping steps, which means the normal conventional way won't capture the actual number of steps<br/>

#### Building a recurrence from an algorithm
$T(n)=aT(\frac{n}{b})+f(n)$<br/>
where:<br/>
- $a$ is the number of recursive calls.
- $\frac{n}{b}$ is the size of each subproblem
- $f(n)$ is the work performed outside those recursive calls


#### Why do we even learn this?
It's useful for:
- Divide-and-conquer algorithms such as merge sort
- Recursive searching, such as binary search
- Recursive tree algorithms
- Recursive matrix multiplication


### 1.3 Amortized Analysis
Amortised analysis determines the cost per operation over a sequence of operations, providing a worst-case guarantee on the sequence without relying on probabilities.<br/>
Because some data-structure operations are expensive only in certain conditions.

#### Amortized vs average-case analysis
- Average-case analysis relies on a probability distribution over inputs or operations.
- Amortized analysis establishes a bound over every permitted sequence of operations, subject 
  to the data structure's rules


## Topic 2: Core Algorithms Design Paradigms
A design paradigm is a general strategy for constructing algorithms. It is not one specific algorithm, rather, it is a reusable approach that can be applied to many different problems.<br/><br/>

### 2.1 Divide and Conquer
Divide and conquer solves a problem by dividing it into smaller subproblems, solving those subproblems recursively, and combining their solutions.
<br/><br/>
The three stages in this method:
1. Divide
2. Conquer
3. Combine the solutions together<br/>

#### Example algorithms:

- Merge sort
- Binary search

  
#### Conditions for effective divide and conquer
- Subproblems are smaller than the original
- Their solutions can be computed recursively
- The subproblems are independent or their dependencies can be managed 
- The combination step is efficient
- The recurrence yields a favorable total cost

#### Limitations:
- Recursion overhead
- Memory consumption
- The possibility that the combination stage is expensive<br/><br/>




### 2.2 Greedy Algorithms 
A greedy algorithm constructs a solution incrementally by choosing what appears to be the best available option at each step.<br/><br/>
A greedy algorithm does not generally explore every possible solution. Instead, it commits to a locally attractive choice, hoping that the sequence of choices produces a globally optimal solution.<br/><br/>
However, a locally optimal choice is not necessarily globally optimal. Greedy algorithms require a proof that their chices preserve the possibility of an optimal solution.


#### 2 important properties:

- ##### Greedy-choice property
  A problem has the greedy-choice property when there exists an optimal solution that begins with a valid greedy choice. After making that choice, the remaining problem can be solved to obtain an optimal overall solution.<br/><br/>This property must be established for the particular problem. It can't be assumed merely because the greedy choice seems sensible.</br><br/>
- ##### Optimal substructure
  A problem has optimal substructure when an optimal solution can be constructed using optimal solutions to appropriate smaller or residual subproblems.<br/><br/>Optimal substructure is also important in dynamic programming.<br/><br/>

#### Greedy graph algorithms:
- Kruskal's Algorithm: Repeatedly selects the lowest-weight edge connecting the current tree to a vertex outside it.
- Prim's Algorithm: Repeatedly adds the lwoest-weight edge connecting the current tree to a vertex outside it
- Dijkstra's Algorithm: Repeatedly finalises the unvisited vertex with the smallest tentative distance, under the assumption that edge weights are non-negative<br/><br/>
### 2.3 Dynamic Programming(DP)
Dynamic programming is a method for solving problems by breaking them into subproblems, solving each distinct subproblem once, and storing the result for reuse. <br/><br/>It is especially useful when subproblems overlap and the problem has optimal substructure.<br/><br/>In some recursive algorithms, the same subproblem may be solved many times. Dynamic programming eliminates this repeated work by remembering previously computed results.<br/><br/>

#### 2 main properties:
- ##### Overlapping subproblems
  Subproblems overlap when the same smaller problem appears repeatedly during the computation.
- ##### Optimal substructure
  A problem has optimal substructure when its optimal solution can be expressed using optimal solutions to suitable smaller subproblems.

#### 2 Implementation approaches
- ##### Memoization: Top-down dynamic programming
  - Begin with a recursive solution.
  - Store the result whenever a subproblem is solved
  - Before solving a subproblem, check whether its result is already stored
  - Return the stored result when available.<br/><br/>
  Memoization often preverses the structure of the original recursive definition.<br/><br/>
- ##### Tabulation: Bottom-up dynamic programming
  - Identify the smallest subproblems.
  - Compute their answers first.
  - Store the result in a table.
  - Use those results to calculate progressively larger subproblems.<br/><br/>
  Tabulation often avoids recursive call overhead and can make memory usage easier to optimise<br/><br/>

  ##### The quality of a dynamic programming solution depends on defining the right states, recurrence, base cases, and computation order.<br/><br/>

### 2.4 Backtracking & Branch-and-Bound
These two methods both explore a search space of candidate solutions, but they use different
criteria to prune the search.<br/><br/>

- #### Backtracking
  Backtracking constructs a candidate solution incrementally and abandons a partial candidate as soon as it violates a constraint or cannot lead to a valid solution.<br/>
  It is naturally represented as a depth-first search tree:
  - Each node represents a partial assignment.
  - Each node represents a partial assignment.
  - A leaf represents a complete candidate or a dead end.
  - A pruned branch is never explored further.<br/><br/>
  Backtracking is particularly useful for constraint-satisfaction problems, where the objective is to find one or all assignments satisfying a set of conditions.<br/><br/>
- #### Branch-and-bound
  Branch-and-bound is primarily an optimisation technique. It searches for the best solution and uses bounds to determine whether a partial candidate could possibly outperform the best solution already found.<br/>
  It has 4 main elements:
  1. Branching: Split the search into subproblems.
  2. Bounding: Compute an optimistic estimate of the best objective achievable within a subproblem
  3. Incumbent: Maintain the best complete feasible solution found so far.
  4. Pruning: Discard a subproblem when its bound proves that it cannot improve the incumbent<br/><br/>

### 2.5 Randomized Algorithms
A randomized algorithm uses random choices during its execution. These choices influence its behaviour, running time, or output.<br/><br/>
Randomization can simplify algorithms, avoid adversarial inputs, and provide strong expected performance. Analysis must account for the probability distribution induced by the random choices.<br/><br/>
#### Las Vegas Algorithms
A Las Vegas algorithm always returns a correct answer, but its running time may vary because of random choices.<br/><br/>
Randomized quicksort is a standard example. It randomly selects a pivot, then partitions the array around that pivot. Different pivot choices produce different partition sizes, but the final sorted array is correct.
#### Monte Carlo Algorithms
A Monte Carlo algorithm has a bounded or otherwise controlled running time but may return an incorrect answer with a specified probability.

#### Types of error:
- One-sided error: Only one type of mistake is possible.
- Two-sided error: Both false positives and false negatives may occur.

#### Why randomisation helps
Randomization can prevent an algorithm from behaving badly on inputs designed to exploit a fixed deterministic strategy. Random pivots in quicksort, random sampling, hashing, and randomized graph algorithms are important examples.<br/><br/>However, randomization does not automatically guarantee efficiency. A randomized algorithm still needs an analysis of its error probability, expected cost, or probability of exceeding a chosen cost threshold.


### 2.6 Approximation Algorithms and NP-hardness
This topic connects practical algorithm design with computational complexity theory. It explains what to do when exact optimisation may require an impractical amount of computation.

#### Approximation algorithms
An approximation algorithm efficiently returns a feasible solution whose quality is guaranteed to be close to optimal.<br/><br/>
For a minimisation problem, let:
- $C$ be the cost of the algorithm's solution.
- $C^{*}$ be the optimal cost.
  
An algorithm has approximation ratio at most $\rho\geq 1$ if:<br/>
$C\leq\rho C^*$

For a maximisation problem, one common convention is<br/>
$C\geq\frac{C^*}{\rho}$

#### P, NP, NP-hard, and NP-complete
- P is the class of decision problems solvable by a deterministic algorithm in polynomial time.<br/><br/>
- NP is the class of decision problems for which a proposed yes-solution can be verified in polynomial time. Equivalently, these problems have certificates that can be checked efficiently.<br/><br/>
- It is not known whether $P=NP$. In particular, the fact that a problem belongs to NP does not mean that it is known to be computationally difficult, nor does it mean that its solutions are impossible to find efficiently.<br/><br/>
- A problem is NP-hard if every problem in NP can be reduced to it using an appropriate polynomial-time reduction. NP-hard problems are at least as hard as all problems in NP under that reduction framework.<br/><br/>
- A problem is NP-complete if it is both in NP and NP-hard.<br/><br/>

## Topic 3: Graph Algorithms
Graph algorithms operate on structures consisting of vertices and edges. They are fundamental to route planning, communication networks, dependency analysis, social networks, scheduling, circuit design, and transportation systems.<br/>
Keywords:

- Vertex (node): An entity represented in the graph.
- Edge: A connection between vertices.
- Directed graph: Each edge has a direction, such as $u\to v$
- Undirected graph: Each edge connects two vertices without a direction.
- Weighted graph: Each edge has an associated value, such as distance, time, or cost.
- Path: A sequence of vertices connected by edges.
- Cycle: A path that returns to its starting vertex without repeating intermediate vertices, under the usual simple-cycle definition.
- Connected graph: An undirected graph in which every vertex can reach every other vertex.
- Connected component: A maximal connected part of an undirected graph.
- Degree: The number of incident edges in an undirected graph. In a directed graph, indegree and outdegree count incoming and outgoing edges separately.

### 3.1 Graph Traversal
Graph traversal is the systematic process of visiting vertices or edges in a graph according to a defined exploration strategy.<br/><br/>
Traversal is useful for determining reachability, identifying connected components, detecting cycles, constructing spanning trees, finding paths, and ordering dependent tasks.<br/>
The two fundamental traversal algorithms are:
- Breadth-first search (BFS).
- Depth-first search (DFS).

#### Breadth-first search(BFS)
BFS explores a graph in layers. Starting from a source vertex, it visits all vertices one edge away before visiting vertices two edges away, then three edges away, and so on.
<br/><br/>
It uses a queue, which follows first-in, first-out order.
<br/><br/>
BFS explores vertices in non-decreasing order of their distance from the source. A vertex is discovered through a predecessor at the preceding distance level. If a shorter path existed, the vertex would have been reachable from an earlier level, and BFS would have discovered it earlier. Therefore, BFS finds a minimum-edge-count path from the source to every reachable vertex.

#### Depth-first search(DFS)
DFS explores as far as possible along a branch before returning to explore another branch. It can be implemented using recursion or an explicit stack.<br/>
DFS can be used to:
- Find reachable vertices.
- Identify connected components in undirected graphs.
- Detect cycles.
- Produce topological order in directed acyclic graphs.
- Find strongly connected components using suitable extensions.
- Classify edges and analyse structural properties of graphs.<br/><br/>
DFS does not generally find shortest paths in an unweighted graph. It prioritises depth, not distance.

### 3.2 Shortest Paths
The shortest-path problem seeks a path between vertices whose total edge weight is minimum.<br/>
A shortest path need not be the path with the fewest edges. A path with more edges can have a lower total weight.<br/><br/>
#### Relaxation
Many shortest-path algorithms use a procedure called relaxation.<br/>
Relaxation improves a distance estimate when a cheaper route has been found. The algorithm's strategy determines when these estimates become final. <br/><br/>
#### Dijkstra's Algorithm
Dijkstra's algorithm finds shortest-path distances from one source to all reachable vertices in a graph with non-negative edge weights.<br/>
Its main idea is to repeatedly select the unsettled vertex with the smallest tentative distance and finalise that distance.
#### Bellman-Ford Algorithm
Bellman-Ford solves the single-source shortest-path problem even when negative edge weights are present, provided there is no negative-weight cycle reachable from the source if finite shortest-path distances are required.
#### Floyd-Warshall Algorithm
Floyd-Warshall solves the all-pairs shortest-path problem, computing the shortest distance between every ordered pair of vertices. It uses dynamic programming.

### 3.3 Minimum Spanning Trees
A spanning tree of a connected, undirected graph is a subgraph that:
1. Includes every vertex.
2. Is connected.
3. Contains no cycles.<br/>
A minimum spanning tree (MST) is a spanning tree with the smallest possible sum of edge weights.
An MST minimises the total weight required to connect all vertices. It does not generally minimise the distance from a particular source to every other vertex. That is a shortest-path-tree objective, which is different.

#### Kruskal's Algorithm
Kruskal's algorithm considers edges in increasing order of weight and accepts an edge if adding it does not create a cycle.<br/>
Procedure
1. Sort all edges by non-decreasing weight.
2. Start with an empty forest in which each vertex is its own component.
3. Consider each edge in sorted order.
4. If its endpoints belong to different components, add it to the forest and merge those components.
5. Stop after selecting \(V-1\) edges.

#### Prim's Algorithm
Prim's algorithm begins from an arbitrary vertex and grows a single tree. At each step, it chooses the minimum-weight edge connecting a vertex already in the tree to a vertex outside it.
<br/><br/>
Prim and Kruskal both produce an MST for a connected, undirected weighted graph. They differ in how they grow the solution:
- Prim grows one connected tree.
- Kruskal grows a forest and joins components.

#### Disconnected graphs
If the graph is disconnected, no spanning tree can connect all vertices. Kruskal's algorithm instead produces a minimum spanning forest, containing a minimum spanning tree for each connected component.<br/><br/>
Prim's algorithm must likewise be restarted in each component if a minimum spanning forest is desired.

### 3.4 Network Flow
A flow network is a directed graph in which each edge has a capacity limiting how much flow can pass through it. The network contains a source \(s\), which supplies flow, and a sink \(t\), which receives it.<br/>
Flow models include:
- Water through pipes.
- Data through communication links.
- Goods through transport networks.
- Assignments between workers and jobs.
- Bipartite matching and resource allocation.

#### The residual network
The residual network represents where additional flow can be sent or where existing flow can be reduced. 

#### Augmenting paths
An augmenting path is a path from source s to sink t in the residual network where every edge has positive residual capacity.

#### The Ford-Fulkerson method
The Ford-Fulkerson method repeatedly finds an augmenting path and increases the flow by its bottleneck capacity.<br/><br/>

The high-level procedure is:
1. Initialise every edge's flow to zero.
2. Construct the residual network.
3. Find an augmenting path from source to sink.
4. Increase the flow by the path's bottleneck capacity.
5. Update the residual network.
6. Repeat until no augmenting path exists.
<br/><br/>

If capacities are integral and augmenting paths are chosen appropriately, each augmentation increases the flow value by at least one unit, so the method terminates for finite integral-capacity networks.<br/><br/>

#### Edmonds-Karp algorithms
Edmonds-Karp is a specific implementation of Ford-Fulkerson that uses BFS to find an augmenting path with the fewest number of edges.<br/>
It avoids the potentially poor behaviour of arbitrary augmenting-path selection and terminates with a maximum flow in a finite graph.

#### Maximum-flow minimum-cut theorem
Flow through any network cannot exceed the capacity of any source-sink cut. Every unit of flow reaching the sink must cross the cut, and the cut's outgoing edges limit how much flow can cross.<br/><br/>

> The maximum-flow minimum-cut theorem states that the maximum possible flow value equals the minimum capacity of any source-sink cut.<br/><br/>
This theorem provides both a way to certify optimality and a powerful connection between two apparently different optimisation problems.

#### Application and reductions
- Bipartite matching
To match workers to jobs, connect a source to each worker, connect workers to the jobs they are qualified for, and connect jobs to a sink.
- Assignment and resource allocation
- Circulation with demands
Additional lower bounds or demand constraints can be handled by transformations to standard flow formulations.
- Minimum cut
Network reliability and partitioning problems can sometimes be represented through cut capacities.

#### Maximum flow vs Minimum cost flow
These are different optimisation problems.
- Maximum flow: Maximise the total amount sent from source to sink, subject to capacities and conservation.
- Minimum-cost flow: Send a required amount of flow, or otherwise satisfy specified supplies and demands, while minimising the total cost.<br/><br/>
In minimum-cost flow, each edge has both a capacity and a cost. A large-capacity route may be more expensive than a smaller-capacity route, so capacity alone is insufficient to determine the optimum.
