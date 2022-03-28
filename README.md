# Data-Structures-in-Python

## Cheat-Sheet

### Search Algorithms-

1. Linear Search:

	Time Complexity: O(n)
	
	Space Complexity: O(1)
	
	
2. Binary Search:

	Pre-requisite: List has to be sorted
	
	Time Complexity: O(log(n))
	
	Space Complexity: O(1)
	
### Tree Algorithms-

1. Binary Search Tree:

	**If tree is balanced:**
	
	Time Complexity: 
	
	Insert: O(log(n))
	
	Find, Update: O(log(n))
	
	List all: O(1)
	
	Space Complexity:
	
	Insert: O(1)
	
	Find, Update: O(1)
	
	List all: O(n)
	
	**If tree is heavily unbalanced:**
	
	Time Complexity: 
	
	Insert: O(n)
	
	Find, Update: O(n)
	
	List all: O(1)
	
	Space Complexity:
	
	Insert: O(1)
	
	Find, Update: O(1)
	
	List all: O(n)
	
	
### Dictionary with hashed map-

1. 


### Sorting Algorithms-

1. Bubble sort-

	**Algorithm-**
	loop n (size of list) times
	start a index 0
	Swap two elements if greater element is previous to smaller element, increment index.
	
	
	Time Complexity: O(n**2)
	
	Space Complexity: O(1)
	
	
2. Insertion sort-

	**Algorithm-**
	Keep the list sorted from left.
	Start at index 1 and iteratively check if the element can be at lower index position.
	
	Time Complexity: O(n**2)
	
	Space Complexity: O(1)
	
3. Merge sort-

	**Algorithm-**
	Use divide and conquer method. 
	Recursively divide the list in two sublists until each list has exactly 1 element.
	The use algorithm to merge two sorted list.
	
	As, each recursive function splits the list, on the function stack, the top function will be run first and 2 elements will be merge sorted, then 2 more lists will be merge sorted, until the stack is empty.
	
	**Average Case**
	
	Time Complexity: O(n**2)
	
	Space Complexity: O(n) --> n elements are stored in n list.
	
	**Worst Case**
	
	Time Complexity: O(nlog(n))
	
	Space Complexity: O(n)
	
4. Quick sort-

	**Algorithm-**
	Start with last element of list as pivot element.
	partition the list, such that all elements less than pivot are in left partition and all elements greater the pivot are in right partition.
	Fix the position of pivot element.
	Now we have [unsorted left list] + [pivot element at correct index] + [unsorted right list]
	By applying divide and conquer strategy we can solve this. such that every recursive call fixes the position of one element(that is pivot element in that call)
	
	
	**Average Case**
	
	Time Complexity: O(nlog(n)) --> Best case when partition is ideal, in each recursive call
	
	Space Complexity: O(n)
	
	**Worst Case**
	
	Time Complexity: O(n**2)
	
	Space Complexity: O(n)
	
	
### Recursion and Dynamic Programming:

1. LCS( Longest Common Subsequence):

	Problem Statement: Given two sequences [ordered collection of characters] find the longest subsequence [sequence obtained after removing one of more characters of parent sequence] that is common in both sequences.
	
	Ex: 
	
	1. 'analogy' and 'alchemy' : lcs = 3
	
	2. 'precipitation' and 'serendipitous' : lcs = 7
	

	3 methods:
	
	1. Recursive Solution:
	
	Time Complexity:
	
	Space Complexity:
	
	2. Recursive Solution with Memoization:
	
	Time Complexity:
	
	Space Complexity:
	
	3. Iterative Solution (Dynamic Programming):
	
	Time Complexity:
	
	Space Complexity:
	
2. 0-1 Knapsack Problem:

	Problem Statement: Find the best set of elements with specific - weight value and profit value associated with each, such that it maximizes the profit and constraint is the weight is no more than the fixed value given called 'Capacity'
	
	Why called 0-1?
	
	Since, each element is either taken or not taken

	
	1. Recursive Solution:
	
	Time Complexity:
	
	Space Complexity:
	
	2. Recursive Solution with Memoization:
	
	Time Complexity:
	
	Space Complexity:
	
	3. Iterative Solution (Dynamic Programming):
	
	Time Complexity:
	
	Space Complexity:
	
### Graph Algorithms:

1. Breadth First Search(BFS):

	**Algorithm-**
	Find all nodes on same level first then find all nodes on level+1 and so on ...
	
	Time Complexity:
	
	Space Complexity:
	

2. Depth First Search(DFS):

	**Algorithm-**
	Find all nodes in one path first, then find new paths.
	
	Time Complexity:
	
	Space Complexity:
	
	
3. Shortest Path Algorithm(Dijkstra Algorithm):

	**Algorithm-**
	
	Time Complexity:
	
	Space Complexity:


	
	
