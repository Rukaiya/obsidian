### Algorithm
An algorithm is a set of well-defined instructions to solve a particular problem.

### Types of Data Structure

Basically, data structures are divided into two categories:

-   Linear data structure
	- Array
	- Stack
	- Queue
	- Linked List
-   Non-linear data structure
	- Graph
		-   [Spanning Tree and Minimum Spanning Tree](https://www.programiz.com/dsa/spanning-tree-and-minimum-spanning-tree)
		-   [Strongly Connected Components](https://www.programiz.com/dsa/strongly-connected-components)
		-   [Adjacency Matrix](https://www.programiz.com/dsa/graph-adjacency-matrix)
		-   [Adjacency List](https://www.programiz.com/dsa/graph-adjacency-list)
	- Trees
		- [Binary Tree](https://www.programiz.com/dsa/binary-tree)
		-   [Binary Search Tree](https://www.programiz.com/dsa/binary-search-tree)
		-   [AVL Tree](https://www.programiz.com/dsa/avl-tree)
		-   [B-Tree](https://www.programiz.com/dsa/b-tree)
		-   [B+ Tree](https://www.programiz.com/dsa/b-plus-tree)
		-   [Red-Black Tree](https://www.programiz.com/dsa/red-black-tree)
		
<table>
	<tr>  
	    <th>Linear Data Structures</th>  
	    <th>Non Linear Data Structures</th>  
	  </tr>
	  <tr>  
		    <td>The data items are arranged in sequential order, one after the other.</td>  
		    <td>The data items are arranged in non-sequential order (hierarchical manner).</td>  
	  </tr>
	  <tr>
	    <td>All the items are present on the single layer.</td>
	    <td>The data items are present at different layers.</td>
	  </tr>
	  <tr>
	    <td>It can be traversed on a single run. That is, if we start from the first element, we can traverse all the elements sequentially in a single pass.</td>
	    <td>It requires multiple runs. That is, if we start from the first element it might not be possible to traverse all the elements in a single pass.</td>
	  </tr>
	  <tr>
	    <td>The memory utilization is not efficient.</td>
	    <td>Different structures utilize memory in different efficient ways depending on the need.</td>
	  </tr>
	  <tr>
	    <td>The time complexity increase with the data size.</td>
	    <td>Time complexity remains the same.</td>
	  </tr>
	  <tr>
	    <td>Example: Arrays, Stack, Queue</td>
	    <td>Example: Tree, Graph, Map</td>
	  </tr>
	 
</table>

### Asymptotic Notations

Asymptotic notations are the mathematical notations used to describe the running time of an algorithm when the input tends towards a particular value or a limiting value.
- The efficiency of an algorithm depends on the amount of time, storage and other resources required to execute the algorithm.

There are mainly three asymptotic notations:

-   Big-O notation
	- Big-O notation represents the upper bound of the running time of an algorithm. Thus, it gives the worst-case complexity of an algorithm.
-   Omega notation
	- Omega notation represents the lower bound of the running time of an algorithm. Thus, it provides the best case complexity of an algorithm.
-   Theta notation
	- Theta notation encloses the function from above and below. Since it represents the upper and the lower bound of the running time of an algorithm, it is used for analyzing the average-case complexity of an algorithm.
### Divide and Conquer Applications

-   [Binary Search](https://www.programiz.com/dsa/binary-search)
-   [Merge Sort](https://www.programiz.com/dsa/merge-sort)
-   [Quick Sort](https://www.programiz.com/dsa/quick-sort)
-   Strassen's Matrix multiplication
-   Karatsuba Algorithm

### Applications of Stack Data Structure

Although stack is a simple data structure to implement, it is very powerful. The most common uses of a stack are:

-   **To reverse a word** - Put all the letters in a stack and pop them out. Because of the LIFO order of stack, you will get the letters in reverse order.
-   **In compilers** - Compilers use the stack to calculate the value of expressions like `2 + 4 / 5 * (7 - 9)` by converting the expression to prefix or postfix form.
-   **In browsers** - The back button in a browser saves all the URLs you have visited previously in a stack. Each time you visit a new page, it is added on top of the stack. When you press the back button, the current URL is removed from the stack, and the previous URL is accessed.

### Enqueue Operation

-   check if the queue is full
-   for the first element, set the value of FRONT to 0
-   increase the REAR index by 1
-    add the new element in the position pointed to by REAR

### Dequeue Operation

-   check if the queue is empty
-   return the value pointed by FRONT
-   increase the FRONT index by 1
-   for the last element, reset the values of FRONT and REAR to -1
