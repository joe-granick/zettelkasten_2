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
Topic: [[Binary Search Trees]]
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
- [[binary search trees]] are **binary trees** differentiated by two additional rules:
	1. each **node** limited to one **left child** and one **right child** 
	2. value of left **descendants** must be less than the value of their **ancestors** and rights descendant nodes must be greater 

#### 251
**tree node** implementation
``` python
# binary tree class stores a value and a left and right child node initialized to none
class tree_node:
	def __init(self, val, left = None, right = None)__:
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
*	If tree is perfectly imbalanced operation could be **O(N)** (eg: tree only has branches going to the right, if value is greater than all nodes search will have to iterate over every single node) 
-  "if there are **n** nodes in a tree, then there are **logN** levels"
- each additional level potentially doubles number of nodes
-  each step moves down a level,  eliminating the preceding level at , meaning all nodes contained in this level are elliminated
- if each level is full, then half of the remaining elements have been eliminated
- [[binary tree search]] has same time efficiency as [[binary search]]  over an [[ordered array]], [[binary tree insertion]] and [[binary tree deletion]] are considerably faster


#### 255
##### Binary Tree Search Implementation
- **trees** are data structure with an arbitrary level of depth, making them well suited for **recursion** 
- **base case:** search value matches the node value, or the node doesn't exist
``` python
def binary_tree_search(node, searchVal):
	#Base case: if node matches or node doesn't exist return the current node
	if node.value == searchVal or node is None:
		return node
	#If search value greater than current node value recurse over right branch
	elif searchVal > node.value:
		if node.right_child:
			binary_tree_search(node.right_child, searchVal)
	#Else search value less than current node value recurse over left branch
	else: 
		if node.left_child:
			binary_tree_search(node.left_child, searchVal)
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

	def binary_tree_insertion(node,insertVal):
		if insertVal < node.value:
			if node.left_child is None:
				node.left_child = tree_node(insertVal)
			else:
				binary_tree_insertion(node.left_child, insertVal)
		
		elif insertVal > node.value
			if node.right_child is None:
				node.right_child = tree_node(insertVal)
			else:
				binary_tree_insertion(node.righht_child, insertVal)
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
Topic: 

Tags: #book
Topics: [[Trees]]
Author: [[Jay Wengrow]]
Year: [[2020]]
URL:https://pragprog.com/titles/jwdsal2/a-common-sense-guide-to-data-structures-and-algorithms-second-edition/#resources

#{{Chapter 1}}

#{{Chapter 2}}

#{{Chapter 3}}

#{{Chapter 4}}

#{{Chapter 5}}

#{{Chapter 6}}

#{{Chapter 7}}

#{{Chapter 8}}

#{{Chapter 9}}

#{{Chapter 10}}

#{{Chapter 11}}

#{{Chapter 12}}

#{{Chapter 13}}

#{{Chapter 14}}

#{{Chapter 15}}

#{{Chapter 16}}

#{{Chapter 17}}

#{{Chapter 18}}

#{{Chapter 19}}

#{{Chapter 20}}
