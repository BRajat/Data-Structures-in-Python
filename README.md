# Data-Structures-in-Python

## Cheat-Sheet

### Search Algorithms-

1. Linear Search:
```

	Time Complexity: O(n)
	
	Space Complexity: O(1)
```
	
	
2. Binary Search:
```

	Pre-requisite: List has to be sorted
	
	Time Complexity: O(log(n))
	
	Space Complexity: O(1)
```
	
### Tree Algorithms-

1. Binary Search Tree:

	**If tree is balanced:**
```
	
	Time Complexity: 
	
	Insert: O(log(n))
	
	Find, Update: O(log(n))
	
	List all: O(1)
	
	Space Complexity:
	
	Insert: O(1)
	
	Find, Update: O(1)
	
	List all: O(n)
```
	
	**If tree is heavily unbalanced:**
```

	Time Complexity: 
	
	Insert: O(n)
	
	Find, Update: O(n)
	
	List all: O(1)
	
	Space Complexity:
	
	Insert: O(1)
	
	Find, Update: O(1)
	
	List all: O(n)
	
```

### Dictionary with hashed map-

1. 


### Sorting Algorithms-

1. Bubble sort-

	**Algorithm-**
	loop n (size of list) times
	start a index 0
	Swap two elements if greater element is previous to smaller element, increment index.
	
```
	
	Time Complexity: O(n**2)
	
	Space Complexity: O(1)
```
	
	
2. Insertion sort-

	**Algorithm-**
	Keep the list sorted from left.
	Start at index 1 and iteratively check if the element can be at lower index position.
```
	
	Time Complexity: O(n**2)
	
	Space Complexity: O(1)
```
	
3. Merge sort-

	**Algorithm-**
	Use divide and conquer method. 
	Recursively divide the list in two sublists until each list has exactly 1 element.
	The use algorithm to merge two sorted list.
	
	As, each recursive function splits the list, on the function stack, the top function will be run first and 2 elements will be merge sorted, then 2 more lists will be merge sorted, until the stack is empty.
	

```

	**Average Case**
	
	Time Complexity: O(n**2)
	
	Space Complexity: O(n) --> n elements are stored in n list.
	
	**Worst Case**
	
	Time Complexity: O(nlog(n))
	
	Space Complexity: O(n)
	
```
	
4. Quick sort-

	**Algorithm-**
	Start with last element of list as pivot element.
	partition the list, such that all elements less than pivot are in left partition and all elements greater the pivot are in right partition.
	Fix the position of pivot element.
	Now we have [unsorted left list] + [pivot element at correct index] + [unsorted right list]
	By applying divide and conquer strategy we can solve this. such that every recursive call fixes the position of one element(that is pivot element in that call)

```	
	
	**Average Case**
	
	Time Complexity: O(nlog(n)) --> Best case when partition is ideal, in each recursive call
	
	Space Complexity: O(n)
	
	**Worst Case**
	
	Time Complexity: O(n**2)
	
	Space Complexity: O(n)
	
```
	
### Recursion and Dynamic Programming:

1. LCS( Longest Common Subsequence):

	Problem Statement: Given two sequences [ordered collection of characters] find the longest subsequence [sequence obtained after removing one of more characters of parent sequence] that is common in both sequences.
	
	Ex: 
	
	1. 'analogy' and 'alchemy' : lcs = 3
	
	2. 'precipitation' and 'serendipitous' : lcs = 7
	

	3 methods:
	
	1. Recursive Solution:
```
	
	Time Complexity: O(2**(m+n))  --> tree root node starts at (m,n) and ends at (0,0) (height of tree = m+n)
	
	Space Complexity: O(m+n)
```
	
	2. Recursive Solution with Memoization:
```
	
	Time Complexity: 
	
	Space Complexity:
```
	
	3. Iterative Solution (Dynamic Programming):
```
	
	Time Complexity: O(m*n)
	
	Space Complexity: O(m*n)
```
	
2. 0-1 Knapsack Problem:

	Problem Statement: Find the best set of elements with specific - weight value and profit value associated with each, such that it maximizes the profit and constraint is the weight is no more than the fixed value given called 'Capacity'
	
	Why called 0-1?
	
	Since, each element is either taken or not taken

	
	1. Recursive Solution:
	
```
	
	Time Complexity: O(2**n) --> each element on one level of binary tree with possibility[taken or not-taken].
	
	Space Complexity: O(n) --> depth-first recursive call stack, stack start poping at level n.
```
	
	2. Recursive Solution with Memoization:
```
	
	Time Complexity: With memoization we can minimize the number of recursive call, O(n*W) --> W = total capacity(every capacity less than equal to W has n dimensional representation of 0's and 1's)
	
	Space Complexity: O(n*W) --> memoized data stored in n-rows and w-columns
```
		
	3. Iterative Solution (Dynamic Programming):
```
	
	Time Complexity: O(n*W)
	
	Space Complexity: O(n*W)
```
	
### Graph Algorithms:

1. Breadth First Search(BFS):

	**Algorithm-**
	Find all nodes on same level first then find all nodes on level+1 and so on ...
	
```
	
	Time Complexity: O(V+E) --> vertices and edges of graph (as each vertex and edge has to be discovered, the number of edges can vary between 1 and V**2 depending on sparsity of input graph
	
			= O(b**(d+1)) --> to find nodes at distance d from start node, where b is average branch out factor.
			
	Space Complexity: O(V) --> vertices of graph
	
```
	

2. Depth First Search(DFS):

	**Algorithm-**
	Find all nodes in one path first, then find new paths.
	
```	
	
	Time Complexity: O(V+E) --> vertices and edges of graph (as each vertex and edge has to be discovered, the number of edges can vary between 1 and V**2 depending on sparsity of input graph
	
			= O(b**(d+1)) --> to find nodes at distance d from start node, where b is average branch out factor.
			
	Space Complexity: O(V) --> vertices of graph
	
```
	
3. Shortest Path Algorithm(Dijkstra Algorithm):

	**Algorithm-**
	Brute force method to find shortest path.
	Initialize distance at start node to zero. 
	Find all neighbour nodes and update their distance from start node. 
	After updatation mark start node as visited.
	Pick next node, which is at minimum distance from start node.
	Consider this next, node as start node and repeat previous steps.
	When destination node is visited return distance, parent and distance of destination node from start node
	
```

	Time Complexity: O(E + Vlog(V))
	
	Space Complexity: O(V) 

```
	
	
