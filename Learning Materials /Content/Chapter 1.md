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
