Added: 202204231010
Name: [[Wengrow 2020]]
Tags: #book
Topics: [[Data Structures]], [[Algorithms]]
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
#### [248]
- [[sort]] algorithms like [[quicksort]] take [[O(NlogN)]] which is still expensive if data needs to be sorted often. 
- [[ordered array]]s have fast read and search maintaining sorted data. However it is slow for inserting and deleting data.
	- Pro: [[O(1)]] [[read]] 
	- Pro: [[O(logN)]] [[search]]
	- Con: [[O(N)]] with O(N/2) average [[insert]] and [[delete]]
-  [[hash table]]s have O(1) search, insertion, and deletion but it does not maintain order
#### [249]
- [[binary search trees]] are a data structure that maintain order and have fast search search, insert, and delete operations
- [[trees]] are a [[node based data structure]] with multiple [[nodes]]
	- [[root node]] a tree's initial node
	- [[parent node]] links to one or more [[child node]]
	- a node's [[descendants]]  are all nodes with the node in question as the root
	- a node's ancestor are all node's from which the node proceeded
	- the root node is the ancestor for all other nodes in the treee [[me]]
	- each row of child nodes make up a tree's [[tree-levels]]
	- [[balnace]] is important porperty of trees

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
![[Wengrowm 2020 Chapter 15 Exercise 1.svg]]
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
5. What order would the tree below print using a [[postorder traversak]]defined by the code below
```python 
#postorder traversal
def traverse_print(node):
	if node is None:
		return 
		
	traverse_print(node.left_child)
	traverse_print(node.right_child)
	print(node.value)
```


## Chapter 16:
Topic: 

## Chapter 17:
Topic: 

## Chapter 18:
Topic: 

## Chapter 19:
Topic: 

## Chapter20:

