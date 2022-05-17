Added: 202204231010
Name: [[Wengrow 2020]]
Tags: #book
Topics: [[data structure]]s, [[algorithm]]s, [[binary search tree]]s, [[priority queue]]s, [[heap]]s
Author: [[Jay Wengrow]]
Year: [[2020]]
Edition: 2nd
URL: https://pragprog.com/titles/jwdsal2/a-common-sense-guide-to-data-structures-and-algorithms-second-edition/#resources
Cite: [[Wengrow 2020]]

## Chapter 1:
Topic: 

## Chapter 2:
Topic: 

## Chapter 3:
Topic: 

## Chapter 4:
Topic: 

## Chapter 5:
Topic: 

## Chapter 6:
Topic: 

## Chapter 7:
Topic: 

## Chapter 8:
Topic: 

## Chapter 9:
Topic: 

## Chapter 10:
Topic: 

## Chapter 11:
Topic: 

## Chapter 12:
Topic: 

## Chapter 13:
Topic: 

## Chapter 14:
Topic: 

## Chapter 15: Speeding up all the things with binary search trees
Topic: [[Binary Search Tree]]s
#### 248
- [[sort]] algorithms like [[quicksort]] take $O(NlogN)$ which is still expensive if data needs to be sorted often. 
- [[ordered array]]s have fast read and search maintaining sorted data. However it is slow for inserting and deleting data.
	- Pro: $O(1)$  [[read]] 
	- Pro: $O(logN)$ [[search]]
	- Con: $O(N)$ with $O(N/2)$ average [[insert]] and [[delete]]
-  [[hash table]]s have $O(1)$ search, insertion, and deletion but it does not maintain order
#### [249]
- [[binary search trees]] are a data structure that maintain order and have fast search search, insert, and delete operations
- [[trees]] are a [[node based data structure]] with multiple [[node]]s
	- [[root node]] a tree's initial node
	- [[parent node]] links to one or more [[child node]]
	- a node's [[descendants]]  are all nodes with the node in question as the root
	- a node's ancestor are all node's from which the node proceeded
	- the root node is the ancestor for all other nodes in the treee [[me]]
	- each row of child nodes make up a tree's [[tree-levels]]
	- [[balance]] is important porperty of trees

#### 250
- [[binary tree]]s defining property are nodes limited to 0 - 2  **child nodes**
- [[binary search tree]] are **binary trees** differentiated by two additional rules:
	1. each **node** limited to one **left child** and one **right child** 
	2. value of left **descendants** must be less than the value of their **ancestors** and rights descendant nodes must be greater 

#### 251
**tree node** implementation
``` python
# binary tree class stores a value and a left and right child node initialized to none
class tree_node:
	def __init__(self, val, left = None, right = None):
		self.value = val
		self.right_child = right
		self.left_child = left
```

**[[binary tree search]] 
1. initialize  **root node** assigned as current node
2. **current node**  value compared to **search value** 
3. `if:` value matches `or` **current node** doesn't exist `return current node`
5. `else:`
	- `if:` value is **greater** than current node repeat operation down **right branch**
	- `if:` value is **less than** than current node repeat operation down **left branch**
6. repeat process until stopping condition met or node reached with no children

#### 252

#### 253
- [[binary tree search]] is fast so long as the tree is **balanced**  
	- since each iteration throws away all nodes descended to the left or right depending on if the value is greater than or less than the node value, a perfectly balanced tree will lose half of the remaining nodes each time if it is perfectly balanced making it naturall  **O(logN)** 


#### 254
##### Binary tree efficiency
*	If tree is perfectly imbalanced operation could be $O(N)$ (eg: tree only has branches going to the right, if value is greater than all nodes search will have to iterate over every single node) 
-  "if there are $n$ nodes in a tree, then there are $logN$ levels"
- each additional level potentially doubles number of nodes
-  each step moves down a level,  eliminating the preceding level at , meaning all nodes contained in this level are elliminated
- if each level is full, then half of the remaining elements have been eliminated
- [[binary tree search]] has same time efficiency as [[binary search]]  over an [[ordered array]], [[binary tree insertion]] and [[binary tree deletion]] are considerably faster


#### 255
##### Binary Tree Search Implementation
- **trees** are data structure with an arbitrary level of depth, making them well suited for **recursion** 
- **base case:** search value matches the node value, or the node doesn't exist
``` python
def bTree_search(node, searchVal):
	#Base case: if node matches or node doesn't exist return the current node
	if node.value == searchVal or node is None:
		return node
	#If search value greater than current node value recurse over right branch
	elif searchVal > node.value:
		if node.right_child:
			bTree_search(node.right_child, searchVal)
	#Else search value less than current node value recurse over left branch
	else: 
		if node.left_child:
			bTree_search(node.left_child, searchVal)
```

#### 256 - 257
- [[binary tree insertion]] is much more efficient than [[ordered array insertion]]
- **binary tree insertion**
1. compare insertion value to root node
2. `if:` value is less than the node value check `check` left child node `else:` check the right node
3.  `if:` child node is `None` insert value `else:` repeat operation until empty child node is found

#### 258
###### Binary  Tree Insertion Implementation
```python

	def bTree_insert(node,insertVal):
		if insertVal < node.value:
			if node.left_child is None:
				node.left_child = tree_node(insertVal)
			else:
				bTree_insert(node.left_child, insertVal)
		
		elif insertVal > node.value:
			if node.right_child is None:
				node.right_child = tree_node(insertVal)
			else:
				bTree_insert(node.right_child, insertVal)
```
- [[binary tree insertion]] is essentially [[binary search]]  with an additional insertions step so it takes $logN+1$ steps [[time complexity]] of $O(logN)$ 
- Insertion provides [[binary search tree]]s a true advantage advantage over [[ordered array]]s,
	- both have the same search  efficiency $O(logN)$  
	- insertion for ordered arrays requires each element after the insertion to be shifted
	-  if inserted at the front this will require $n + 1$  operations with a time complexity of $O(N)$ 
- The efficiency of insertion becomes a significant concern if the data in an application is ecpected to undergo frequent changes

#### 259 - 260
###### Insertion Order
- trees will only maintain balance with insertions from randomly ordered data
- insertion from ordered data will dirsupt the balance, and deteriorate efficieny toward $O(N)$ worst case scenario 
- data should be randomly before converting an [[ordered array]] to a [[binary search tree]] sorted 
- random insertion is the typical situation or **average case**

#### 260 - 271
##### Deletions
- [[binary tree deletion]] is more complicated
- Potetnial situations
	- `if:` deletion node has no children it can be deleted
	- `if:` node has one child delete node and replace with child node
	- `if:` node has two children  need to find an replace with a [[successor node]]
	- `search`  all left child descendants of the deleted nodes right child, the bottom valu becomes the successor node
	- `if` successor node has right child assign as left child of former parent of successor node
##### Finidng the successor node
- [[successor node]] is the node with the minimum value out of the set of all nodes greater than the value of the deleted node
- finding the successor becomes tricky when deleted node is high up
> 1. visit right child of deleted node, all subsquent children will by definition be greater than the deleted node, due to the imposed constraints on binary search tree insertion
> 2. from that node visit each subsquent left child until last descendant is reached
> 3. replace deleted node with successor node
> 	1. `if:` successor node has right child replace successor node with orphaned descendant

##### Deletion implementation
```python


def bTree_delete(node, deleteVal):
	# base case
	if node is None:
		return None
	
	elif deleteVal > node.value:
		bTree_delete(node.right_child, deleteVal)
		return node
		
	elif deleteVal < node.value:
		bTree_delete(node.left_child, deleteVal)
		return node
	
	elif node.value == deleteVal:
		# if left child doesn't exist return right child as successor
		# if right also nonexistent child will be returned as None as per base case
		if node.left_child is None:
			return node.right_child
		
		# if right child doesn't exist return left child as successor
		elif node.right_child = None:
			return node.left_child
		
		#if node has two children call successor function to find replacement
		else:	
			node.right_child = successor(node.right_child, node)
			return node

def successor(node, deleteNode):
	#if node has left child recursively call function down left subtree
	if node.left_child:
		node.left_child = successor(node.left_child, value)
		return node
	
	# if node has no left child, then current node is successor
	# make node value the new value of the node to be deleted
	else:
		deleteNode.value = node.value
		# successor node's right child returned as parent's left child
		return node.right_child
```

###### successor function explained
after passing current nodes right child and the node itself
1. Find successor node
2. overwrites value of current node with value of successor node,
	-  not moving node just overwiting value
3. original successor node deleted by moving successor nodes right child to it's parent node's left child
4. returns original `right_child` or `None` if original `right_child` ended up serving as it's own sucessor node (if its own `left_child` is `None`)
return value of `successor()` become's current node's right child. This either:
	- leaves right child alone
	- changes it to `None` if right child was used as succesor

[[binary tree deletion]] has the same time complexity of [[binary tree insertion]] and has the same efficiency advantage over [[ordered array deletion]] 

#### 272 - 277
##### Traversal
- [[binary search tree traversal]] visits each node within a tree, can be used to perform some,  operation while there
	- traversing just means accessing each node
- by definition traversal has a time complexity  $O(N)$ as every node needs to be visited
- binary search tree traversal can be done in alphabetical order as demonstrated in the code block implementation below
	- recursive implementation natural here
- traversal imporatant operation for node based data structure, with more complex algorithm traversal implementation adapted fro [[graphs]]

```python 
def traverse_print(node):
	if node is None:
		return None
	
	traverse_print(node.left_child)
	print(node.value)
	traverse_print(node.right_child)
```

##### Exercises
1.  Insert following array of number into an empyt binary search tree. What does the resulting tree look like?
![[Wengrow 2020 Chapter 15 Exercise 1.svg]]
2. What are the mac number of steps needed to search for a value in a well balanced binary search tree?
	- Answer: $log_{2}1000$ takes 10 steps  
3. Write an algorithm that finds the maximum value in a Binary Search Tree
	- Answer: this just requires finding the rightmost child node
```python
def bTree_max(node):
    if node.right_child:
        bTree_max(node.right_child)
    else:
        return node.value
```

4. What order would the rtee below print using a [[preorder traversal]] defined by the code below
```python 
#preorder traversal
def traverse_print(node):
	if node is None:
		return 

	print(node.value)
	traverse_print(node.left_child)
	traverse_print(node.right_child)
```
![[binary search tree preorder traversal.svg]]
5. What order would the tree below print using a [[postorder traversal]]defined by the code below
```python 
#postorder traversal
def traverse_print(node):
	if node is None:
		return 
		
	traverse_print(node.left_child)
	traverse_print(node.right_child)
	print(node.value)
```
![[binary search tree postorder traversal.svg]]

## Chapter 16: Keeping your priorities straight with heaps
Topic: [[heap]]s, [[priority queue]]s

#### 279
**heaps** are a tree data structure particularly useful when leatest or great element needs to be tracked 


##### Priority Queues
- [[priority queue]] *deletion* and *access* work [[FIFO]] like a normal **queue**
	- data accessed and removed from **front only**
- *insertion* work like an **ordered array** 
	- maintains sort order
	- e.g. ER triage prioritizes by severity of symptoms

#### 280 - 283
##### heaps
- **heaps** more efficient way to implement **priority queue** than **ordered arrays**
- specifically use a [[binary heap]]
	- type of **binary tree**
	- [[max heap]] or [[min heap]], both work the same way but opposite
- heap maintains following conditions
	1.  [[heap condition]]: each node must be greater than all descendants (or less than in the case of a **min heap**)
		- differs from *binary search tree* since a node will never have descendants greater than it 
	2. [[complete tree]]: all nodes in row must be filled before moving to next row 
		- bottom row can have empty nodes as long as no node to the right of empty node

![[heap condition.svg]]

![[complete trees.svg]]
#### 284 -
##### heap properties
- heaps are [[weakly ordered]]
	- weak ordering not useful for search as it is unclear whether value among right or left descendants
- root node is always the greatest (or least in the caase of *min heap*) valued node
	- this makes heaps ideal for implementing priority queues
	- priority queues alwasy want to access greatest (or least) node value 
	- root node represent node with highest priority
- heap has two primary operations 
	1. [[heap insert]] 
	2. [[heap delete]]
	- optionally can have read operation
	- search is not effective, and typically not an operation for heaps
- heaps have a[[last node]], the rightmosty node in the bottom level
##### 285 -287
###### heap insertion
insertion algorithm steps
1. create node with new value and insert into first available rightmost spot in bottom row, this now becomes the **last node**
2. compare new node with parent bnode
3. `if:` new node is greater `swap:` with parent node
4. `repeat:` until nodes parent has value greater than the inserted node
- process [[trickle]]s up node until placed in location with parent greater than value
- *heap insert* has efficiency of $O(logN)$ 
	- by nature tree is organized into $logN$ rows
	- each move up eliminates half of remaining elements
	- worse case scenario have to insert into top row, taking $logN$ steps at most
![[heap insertion.svg]]



##### 287 - 288, 293 -
###### problem of finding the last node
- all that can be seen is root node, and heap can only be traversed through links from node to node
- problem in finding **last node** without having to searh through all nodes

##### 288 -292
###### heap deletion
- important to note that for heaps **root node**  is only node ever to be deleted
	- this is exactly what is needed for a **priority queue**

deletion algorithm steps
1. `replace:` **root node** value with value of **last node**
2. `trickle down:`  new **root node** to proper location
	1.  check if either existing child node is greater than the **trickle node**
		-  if at least one is swap with root node
		- repeat with children nodes until no child node remains that is greater than the trickle node
- time complexity of $O(logN)$ as in worst case all node will need to be trickled through all *levels* and be placed in the last level
	- a heap has $logN$ levels with $N$ being the number of nodes

![[heap deletion.svg]]
- process [[trickle]]s node up until placed in location with parent greater than value
- *heap insert* has efficiency of $O(logN)$ 
	- by nature tree is organized into $logN$ rows
	- each move up eliminates half of remaining elements
	- worse case scenario have to insert into top row, taking $logN$ steps at most
##### heap consistency between insertion and deletion outweigh faster insertion of ordered arrays for priority queues
the efficiency of heaps make them a better choice for implementing priority queues
|           | ordered array | heaps     |
|:--------- |:------------- |:--------- |
| insertion | $O(N)$        | $O(logN)$ |
| deletion  | $O(1)$        | $O(logN)$ |

while *ordered array insertion* is very fast with $O(1)$ deletion for deletion *ordered array insertion* is **slow** with time complexity $O(N)$ 

*heap insertion* and *heap deletion* are both consistently fast with time complexity $O(logN$)
|           | ordered array  | heaps |
|:--------- |:-------------- |:----- |
| insertion | slow           | fast  |
| deletion  | extremely fast | fast  |

- for common use cases insertions and deletions occur in close to equal frequency
- with insertions equal to deletions the consitency of heaps is preferable because it will be consistently very fast for the priority queues primary operations
	- heaps are optimized for 
- the slow speed of array insertion slows down entire operation to the speed of the worst case operation
- example would be an emergency room triage where patients are going in at an equal rate of being removed, if faster removal can't be performed until recieval is finished it will slow down serving patients to the doctor to the rate of receival because it is just as likely to be occuring
##### implementing a heap with an ordered array is a common way to solve the issue of tracking the last node
- insertion requires placement into last node and deletion starts with replacing the root node with the last node
- linked node based data structures like trees can only see the node it is connected too, so to find the last node requires searching every node which has a time complexity of $O(N)$
- insertion can't just place node anywhere (always to the left most node) and deletion can't just replace the  the root node with the next node to arbitrarily (always with the right child for example) because it violates the heap's **completeness** constraint
- completeness is critical to the heap's benefits because it guarentees the heap will be **well-balanced**
- a **well-balanced** tree limits the growth of level to $log(N)$ levels for ever $N$ node
![[incomplete heap insertion deletion imbalance.svg]]

##### using ordered arrays to implement heaps is a common abstraction that efficiently keeps track of the last node, which is critical to the priority queue's most common operations *insertion* and *deletion* [295], [296]
- finding the last node is critical to the heap's operations
- ordered arrays are an efficient way to keep track of the last node
- even though heaps are naturally expressed as independent linked nodes the heap can actually just finction as an abstract data type traversing the array as if the indexes were individual nodes, and tracking the relationship between them as function to define the parents and children
![[heap ordered array implementation.svg]]
- each node is assigned an index in the array
- assignement works in pattern of going top down and left to right
	- root node is always at index 0
	- last node is always last element in the array

##### arrays are used for heap implementation because they solve the "problem of the last node" [296]
- with an array the last node will be the last element and is trivialy to access instantatneously
- insertion is done at the end as well, then trickled up accordingly maintaining the last node as the last indexed element
```python
### class heap to be implemented
```
- ordered arrays aren't the only way to solve this problem, although  it is the most common implementation [301], [302]
	- linked lists can be used ti implement heaps, solving the [[problem of the last node]] using binary numbers [301]
	-  
##### traversing a heap with nodes is straightforward, but with a functionaly ruleset and maintenance of the pattern of insertion,  the parent index of a node and child indices can be simply calculated, forgoing need to directly access a link [297]
- pattern of top down left to right allows child and parent node indexes to be calculated as the following will always be true
	- `left_child_index = (node_index *2) + 1`
	-  `right_child_index = (node_index *2) + 2
	- `parent_index = floor((node_index-1)/2)
	- since these formulas are deterministic the array can be treated as functionally the same as a tree

##### heap is first example of a tree structure that benefits from implementation with ordered arrays [302]
- any type of binary tree can be implemented using an array, but the heap is the first one where the structure is advantageous, allowing constant access to the last node
	- why would [[binary search tree]]s not benefit?

##### heap is a natural fit to use for priority queues as it gives immediate acces to the max value (or min value) items and priority queues need main function is to access the highest priority item [302]
- heap's root node is assigned highest priority node value, giving immediate access to this value
- once value is served, next highest priority replaces it

##### the **weakly orderded** structure imposed by the by the heap property is the main advantage, maintaining consistently fast insertion and deletion speed [302]
- while ordered arrays have fast deletion insertion is slower by an order of magnitude as it needs to be perfectly ordered requiring each index to be shifted $O(N)$ in worst case scenari
- both heap insertion and deltion are fast as ordering doesn note need top be perfect. 
	- levels maintain rank order, but nodes do in the same level can be inserted in th next available spot
	- this imperfect or *weak* order means in worst case scenario the node needs to be shifted through each level
	- since there are only $logN$ levels for every $N$ element insertion will have worst case time complexity of $O(logN)$
 




##### priority queue uses
- certain implementations of Dijkstra's Shortest Path algortithm
- dynamically fetch next best or next worse elements
- huffman encoding (used for lossless data compression)
- breadth first search (BFS) algorithms like A* use priority queues to continuously grab next most promising node
- minimum spanning tree (MST) algorithms
https://www.youtube.com/playlist?list=PLDV1Zeh2NRsCLFSHm1nYb9daYf60lCcag





## Chapter 17: It doesn't hurt to trie
Topic: [[trie]]s 

##### tries are a less common tree data structure that are well structured form any text based tasks like auto-complete approaching $O(1)$ time complexity [305]
- to have info available to return for autocomplete suggestions, data structure needs to store all combinations of letters branching from each path letter
- if this "dictionary" were stored in an unordered array search would be $O(N)$ with all the branching paths the $N$ for this data structure is very large and brute force array search would take very long
- stored in an ordered array [[binary search]] fares better providing a time complexity fo $O(logN)$, but still not ideal
- tries achieve close to $O(1)$ and can be used for text based operations like autocomplete and autocorrect as well as otherapplications that involve :
	- ip address
	- phone number

##### tries consist of collections of nodes that oint to other nodes like all trees, but unlike binary tress can have an unlimited number of children[306]
- for autocomplete each **trie node** contains a [[hash table]] with english characters as keys and values of the child node hash tables, which then point to the hash tables of their children
[[trie node.svg]]
```python

# trie node contains hash table of child
class TrieNode:
	def __init__(self):
		self.children = {}

#trie class keeps track of root node
class Trie:
	def __init__(self):
		self.root = TrieNode()
```



## Chapter 18:
Topic: 

## Chapter 19:
Topic: 

## Chapter20:

