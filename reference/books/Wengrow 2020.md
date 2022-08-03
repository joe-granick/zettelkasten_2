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
- [[Trees]] are a [[node based data structure]] with multiple [[node]]s
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
![[trie node.svg]]

- right now the trie only has one path for each letter sequence, but can add more children to create more word paths [308]
- "act" could be encoded by adding "t" as a descendant of "a" in the root level [308]

![[trie branching word paths.svg]]
- tries can be visualized in a more stripped down way shown below [309]
![[trie stripped down diagram.svg]]


```python
#page 307
# trie node contains hash table of child
class TrieNode:
	def __init__(self):
		self.children = {}

#trie class keeps track of root node
class Trie:
	def __init__(self):
		self.root = TrieNode()
```

##### using the asterisk as a key in paths contaning "russian doll words" is crucial for indicating when a word has ended, otherwise wods that contain other words may be ambiguous, it indicates what parts of words are words themselves [310]
- storing the words "bat" and "batter" poses a problem, as "batter" contains "bat"
- asterisk needs to be placed as key in tree level that contains the second "t"
	- first "t" will point to a node that contains the hash table with "\*" and terminates there as well as "t" and it's children
- this allows the trie to return "bat" as a potential suggestion while still allowing the path to continue to return "batter" as well
![[trie prefixes words within words.svg]]
- most autocmplete tries contain data representing 1000s of the most commonly used words, so tree becomes more complicated but operates in the same fashion
##### [[trie search]] is the primary trie operation and can be implemented to find only *complete* words or *prefixes* as well [311]
- both version of search are similiar, [[prefix search]] will find complete words as well as prefix words because a complet word is at least as valid as a prefix
##### Trie search steos
1. initialize `current_node` as the tree's root node
2. iterate over each character in the search string
3. each iteration evaluate if `current_node` has child with that character as a key
	- if character is not a key in child dictionary node return `None`, string does not exist in trie
	- if character is a key in child node 
		- set `current_node` to be child node
		- return to step 2 and repeat over next character in search string
	4. if end of search is reached search string has been found in trie

**Setup:** `current_node` initialized to root node and point to first letter in string [311]
 **Step 1:** "c" is a child key of root, `current_node` is now set to be the that key's value, which is the child node's dictionary. Iterate thorugh string by pinting to next character "a"  [311],[312]

   ![[trie search setup.svg]]
**Step 2:** "a" is a child key of  `current_node` repeat previous step so current node is set to child node and point to next character in string "t"[312],[313]

![[trie search step 1.svg]]
**Step 3:** pointing to character "t" in search string check if `current_node`, it does and follow down to next child [312],[313]
![[trie search step 3.svg]]
**Finish:** end of string has been reached meaning "cat" is contained in the trie[313]
![[trie search complete.svg]]
##### trie search implementation [313], [314]
``` python
def trieSearch(self, search_word):
	current_node = self.root
	for char in search_word:
		if current_node.children.get(char):
			current_node = current_node.children[char]
		else:
			return None
	return current_node


```
- if loop makes it through string word has been found in tree and `return current_node`
	- return the node instead of true to help with autocomplete
	- this is so autocomplete starts collecting words at the prefix's last node collecting all words from there
	- otherwise collection would have to start searching at root node [327]

##### trie searches grow with the size if the input rather than the size of the data structure with incredibly efficient time cimplexity of $O(K)$ [315]
- trie search algorithm is very efficient as each character is stored in a hash table with $O(1)$ search
-  this makes search very efficient compared to the size of the data stucture
	- much more efficient than $O(logN)$ binary search on an ordered array
- search time increases with the size of the search string, not the amount of data in the data structure taking only as many steps as number of elements in string ("cat" requires 3 steps)
- since search time increases with size of data structure it will not have an efficiency of $O(1)$ as it grows with the size of the input, but classifying it as $O(N)$ would be misleading as it is much faster and $N$ refers to the number of elements in the data structure
- trie search therefore has time complexity of $O(K)$ where $K$ is the size of the input string . This isn't constant $O(1)$ since the string can vary, it is similiar to constant time because it isn't affected by the size of the data structure. This means the trie can be very large and not affect search speed
	- a string of 3 characters alwasy takes 3 steps
- speed of algorithm is not affected by the size of all data avaliable, only size of the input making it extremely efficient

##### tree insertion is needed to populate a tree and operates similarly to search [316]
1. initialize `current_node` variable to root node
2. iterate over each character in search string
3. check if current node has child with  character as key
4. if it does assign child as `current_node` and repeat step 2 with next character in string
5. if character is not a child node 
	-  create child node with character assigned
	- assign new node to be `current_node`
	- repeat step 2 with next character in string
6. when last character is inserted add a "\*" as child node of last node indicating word is complete
- insertion starts off like search and only diverges when `current_node` doesn't have a child with current character as a key [320]
	- at this point current charavcter is added as a new [[key-value pair]] in current node's hash table
	- key is current character and value is new `TrieNode()`
- insertion require $K + 1$ steps (+1 for "\*") giving a time complexity of $O(K)$[320] 
```python
def trie_insert(self, word):
	current_node = self.root

	
	for char in word:
	#insertion works like search as long as the character is already 
	#contained in tree
		if current_node.children.get(char):
			current_node = current_node.children[char]
	#when character doesn't exist insertion adds it as a key-val pair
	#in the current nodes child hash table
		else:
	#current character becomes key and new TrieNode is value
			new_node = TrieNode()
			current_node.children[char] = new_node

	#new node now set as current node
			current_node = new_node

#once loop completes and all characters inserted, "*" to last node's #hash table with value of None
	current_node.children['*'] = None 
	
	
```
##### autocomplete benefits from addition of a recursive collection function, to gather all word branches starting from the last node of the search term [320]
```python
#current node used as first parameter
def collectAllWords(self, node = None, word = '', words = None):
#if words assigned [] in default it will return same list every time
	if words is None words = [] else words

	#if node doesn't exist assign root node
	current_node = node or self.root
	#iterate over all descendant nodes
	for key, child in current_node.children.items():
		#if child is * that means that word is complete
		#complete word added to the array
		if key == "*":
			words.append(word)
			
		else:
		#recursively call on child node, combine word with each letter
		#each recursive call uses separate copy of string
			self.collectALLWords(self, child, word + key,words)
			
	return words	
```
- in book words has default argument assigned to \[\], but this would be incorrect as each time it is called it will use the same list (each time collectAll values is called, new list is appended to previosu list calls)  [[default parameter values in python]]
- simpler function that collects all words starting at the input node and listing all the words that descend from that node [320]
- don't necessarily want to display all suggestions, but want to have them available [320]
- `node` specifies the node to start with, becoming the root for all possible words that can be created with node as a  prefix[321]
	- if no node is provided, will start with root node and collect every possible word in the trie
- as each recursive copy of word`word` reach complete node"\*" for completed words, can be added to `words` array which is what is returned when function completes [321]
- function loops over all key-value pairs where `key` is a single character in child hash table and `value` is the next child node
- `self.collect_words(self, child, word + keyChar, words)` this function recursively calls next node in sequence and adds current node key `keyChar` to the current `word` string object [322]
- the `words` array collects each completed word, where the recursive call terminates each time the next child is '"\*" the `word` strings is appeneded [322]
- `words` array is returned when all recurisve calls terminate, if deafult root node is the first node then all words are returned in array [322]
- function works recursively because  of the difference of how strings are stored in memory vs how arrays/hash tables are stored in memory [322]

##### recursion walkthrough
**Call 1:** 
- current node defaults to root, word is empty string, and words is empty array.[323]
![[collect words call 1.svg]]
- iterate over root node's children, this node only has one child "c"[323]
- current calll added to call stack [323]
- recrusively call `collectAllWords` on "c" child node 
- string "c" passed to argument `word + key` adding the key of the child node to currently empty strung
- words array passed in argumenty, still empty string 
- below displays where trie is once call is made
![[collect words call 1 call stack.svg]]
**Call 2:**
- iterate over current node's children[323]
- only one child key "a"[323]
- add current call tothe call stack[323]
- recurively call `collectAllWords` on child "a" node[324]
- "a" key from child node added to currenrt word "c" in `key + word` argument[324]
- word still passed as empty string[324]

![[collect words call 2.svg]]
**Call 3:**
- iterate over current node's children "n" and "t"[324]
- add current call to call stack [325]
- cuurent node"n/t" node as it has "n" and "t" as children[324]
- call `collectAllwords` on "n" children with `word` passed as "can" from "ca" `word +` "n" `key`
![[collect words call 3.svg]]
**Call 4:** 
- iterate over current node's children  which is one"\*" meaning words has ended[325]
- base case reached add `word` "can" to `words` array [324]
![[collect words call 4.svg]]
**Call 5:**
- pop top call from stack which was "n/t" node with word "ca"
- now return to the call [325]
	- return to a recursive call every time it is popped[324], [recursion chapter]
- call is still with `word` "ca" but `words` array maintains the "can" having been passed up the call stack after the previous call finished [325]
	- this works due to the difference in how arrays and strings are handled in memory [325], [dynamic programming chapter?]

![[collect words call 5.svg]]
**Call 6:** 
- "n" has been iterated over, now loop over "t" key [325]
- add current call to call stack for second time [325]
- recursively call `collectAllWords` on "t" child node [326]
- `word` "ca" `+ key` "t" passed as "word" argument, and array \["can"] passed as `words` [326]
![[collect words call 6.svg]]
**Call 7:**
- iterate over current "t" node's children [326]
- only child is "\*" maining base condition is reached and current `word` "cat" added to `words` array[326]
- call stack now unwound popping each call finishing their execution returning the `words` array at each call until all are finished and final call return is array containing all words in the trie [326]
![[collect words call 7.svg]]

##### strings create separate copies in memory which allows separate words to be created from each child [325]
- arrays and hash table are modified in the same memory location, therefore they can be passed up and down the call stack and can be used for dynamic programming as different recursive branches of the function can access them [325]
- in contrast each time a string is called a separate copy is created in memory [325]
- therefore each recursive branch has a different copy of the string, each branch in  prefix will be mainatined in memory and nodes (letters) can be added in each call and created as separate objects
- since the array containing the words is the same object in memory each separate string object is added to the same array no matter where their recursive call ends [[Granick-2022-05-20]]




##### autocomplete can find any prefix by combining trie search with collectAllWords [326]
- autocomplete takes whatever string a user types ina as a parameter `prefix` upon which it performs a search, then constructs a list starting at the child node of the last letter in the o `prefix` input string [327]
```python
def autcomplete(self, prefix):
	currentNode = self.trieSearch(prefix)
	if not currentNode:
		return None
	else:
		return collectAllWords(currentNode, prefix)
	
```
- serch trie for prefixm if it doesn't exits `None` returned
- if prefix does exist search returns node of last letter in prefix and it is assigned as the current node[327]
	- - possibly add function the inserts word once user completely types it out and `None` is retunred by the autocomplete? [[Granick-2022-05-21]]
- `collectAllWords` called starting with the current node and the prefix in the word argument, adding all child descending from that node to words array[327]
- fonce `collectAllWords` call finished array returned is returned by the `autocomplete` function
- this array can then be dispalyed to the user if desired

##### autcomplete works better if the most popular words are tracked and display is prioritized [327]
- if every word combination were displayed, a trie witha even a moderate dictionary could become unusable due to an oevrwhelming amount of words displayed[327]
- therefor a better user experience can be created by limiting the number of words displayed[327]
- good way to limit the number of words displayed is by prioritizing by popularity[327]
- to display most popular words, need to track the frequency of use
- currently the termination "\*" only stores a null value, but it can track frequency by storing a count that can store a popularity score instead [327]
- using numbers as the value for the "\*" store their scores along with them and sort in order of their popularity
	- would this make sense for a priority queue? [[granick]] 

![[autocomplete tries with values.svg]]
```python

class trieNode:
    def __init__(self):
        self.children = {}

class trie:
    def __init__(self):
        self.root = trieNode()

    def search(self, word):
        currentNode = self.root
        for char in word:
            if currentNode.children.get(char):
                currentNode = currentNode.children[char]
            else:
                return
        return currentNode

    def insert(self, word):
        currentNode = self.root
        for char in word:
            if currentNode.children.get(char):
                currentNode = currentNode.children[char]
            else:
                newNode = trieNode()
                currentNode.children[char] = newNode
                currentNode = newNode
        currentNode.children["*"] = None

    def collectAllWords(self, node = None, word = "", words = None):
        words = [] if words is None else words
        # start at beginning if no node passed in
        currentNode = node or self.root
        for key, child in currentNode.children.items():
            if key == "*":
                words.append(word)
            else:
                self.collectAllWords(child, word + key, words)
        return words

    def autocomplete(self, prefix):
        startNode = self.search(prefix)
        if not startNode:
            return None
        return self.collectAllWords(startNode, prefix)

    def traverseAndPrint(self, node = None):
        currentNode = node or self.root
        for key, child in currentNode.children.items():
            print(key)
            if key != "*":
                return self.traverseAndPrint(child)

    def autcorrect(self, word):
        currentNode = self.root
        prefix = ''
        for char in word:
            if currentNode.children.get(char):
                currentNode = currentNode.children[char]
                prefix = prefix + char

            else:
                return self.collectAllWords(currentNode, prefix)[0]
        return word

  
test = trie()
insert_words =["ball","bald","balance",
				"balter","banter","attack",
				"cat","catnip","catnap"]
for word in insert_words:
	test.insert(word)

print(test.collectAllWords())
print(test.autocomplete("b"))
print(test.autocomplete("ban"))
print(test.autcorrect("carnap"))
```

```python
def hello(name):
	print(name)

if __name__ == "__main__":
	hello("Eve")
```
## Chapter 18: Connecting everything with graphs
Topic: [[graphs]],[[breadth first search]], [[depth first search]], [[djisktra's shortest path algorithm]]

##### graph strcuture is well suited to storing network data like the type of relationships you would need to model for a social meida network [331]
- when storing relationships, it could be loguically represented as a two dimensional array, each subarray contains a pair of name representing a frienship [331]
```python
friendships = [
			   ["Alice", "Bob"],
			   ["Bob", "Cynthia"],
			   ["Alice", "Diana"],
			   ["Bob", "Diana"],
			   ["Elise", "Fred"],
			   ["Diana", "Fred"]
			   ["Fred", "Alice"]
]
```
- with a set up like this an algorithm would need to look through all elements to determine if a person is another person's friend which has a time complexity of $O(N)$[331]
- graphs can return [[adjacent vertex]] in $O(1)$

##### graphs are specifically well suited to networks fo relationships as they naturally model connections [332]
![[Graph Data Structure.svg]]
- graph represents a social network  [332]
- each person represented by a node [332]
	- a node in graph terminology is a [[vertex]] [333]
- connections are represented by links or [[edge]]s  [333]
	- edges are the relationship between vertices in a graph

##### trees are a subset of graphs with additional contstraints for completeness and acyclic
- trees and graphs are both abstract data types made up of linked nodes
- trees are a specific type of graph with the requirements of being [[connected graph]][333] and cannot have [[cycles]][332] 
##### edges in a directed graph vertex relationships only work one way, unless cyclical relationship defined xplicitly with additional edge [334]
- in a social network "alice" may follow "bob", but "bob" doesn't necessarily follow back[334]
	- if he does a separate edge create from bob to Alice (like with Bob and Cynthia in diagram)[334]
![[directed graph.svg]]
##### object-oriented graph implementation [335]
```python
class Vertex:
    def __init__(self, value):
        self.value = value
        self.adjacent_vertices = []
#adds a directed edge between node and neighbor
    def add_adjacent(self, neighbor_vertex):
        self.adjacent_vertices.append(neighbor_vertex)
#adds an undirected edge between node and neighbor
    def undirected_add_adjacent(self, neighbor_vertex):
        if neighbor_vertex not in self.adjacent_vertices:
            self.adjacent_vertices.append(neighbor_vertex)
            neighbor_vertex.undirected_add_adjacent(self)

joe = Vertex("Joe")
bob = Vertex("Bob")
joe.undirected_add_adjacent(bob)

for vertex in joe.adjacent_vertices:
    print(vertex.value, " is Joe's friend")

for vertex in bob.adjacent_vertices:
    print(vertex.value, " is Bob's friend")
```

##### with a connected graph access to one vertex means all other vertcies can be reached, however may not hold true for disconnected graphs [336]
- with connected graphs this `Vertex` class can achieve all algorithms [336]
- with a [[disconnected graph]] will need to store all graph vertices in separate data structure like an array[336]
	- often implememted with a `Graph` class that contains the array

##### adjacency lists store a vertex's adjacent vertices in an array, while adjaceny matrices use a two dimensional array, both implemenations advantages/disadvantages for diffenrent situatiosn [336]
##### [[graph search]] is the primary graph operation [337]
- operates a little differently than most other search [337]
- in most contexts a search operation ivolves finnding an element wiothin data structure [337]
- search in the context of graphs involves fining one particular vertex  starting at another vertex [337]
- sequence ofof edges traversed from one vertex to another is the [[path]]
- multiple paths can exist betwenn vertices [338]
- graph search use cases [339]
	- finding a specific vetex within a graph
		- in a [[connected graph]] search can find any vertex from any other vertex
	- finding whether two vertices are connected 
		- path exists where one vertext can be reached from another just by traversing edges to neighbors
	- search can be use to traverse every vertex in a graph
		- useful if an operation needs to be performed on each vertex
- most common methods for traversing graph  are [[depth-first search]] (DFS) and [[breadth-first search]] (BFS) [339]
- some graph algorithms attempt to find the [[shoretst path]]

##### depth first search
- works similiarly to [[binary search tree traversal]] [272] and [[file system traversal]] [156]
- graphs differ because they have cycles which would lead to an infinite loop[339]
- **DFS** requires keeping track of visited vertices and preventing them from being evisted so that algrothm doesn't run infinitely[339]
- hash table can be used to store verticeas already visted[340]
	- each time a vertext visted addad as a Key-Value pair in table[340]
	- if it is in table emans it ahs been visited and will indicate that algrothm should ignore that vertex [340]
###### DFS traversal
- graph traversal similiar but simpler implementation than tryin to find path from one particular vertex to another [339]
**steps**
1. start at any vertext in graph
2. add vertex to visted vertices hash table
3. iterate through each [[adjacent vertex]]
4. `if` vertex is in hash table move to next vertex
5. `else` vertex hasn't been visited recursively call **DFS** on adjacent vertex
![[depth-first search.svg]]
##### DFS code implementation
```python
#depth-firsts search traversake
#simpler version that just finds all vertices
    def dfs_traverse(self, visited = set(), path = ""):
        #each path recorded as a string
        #each recursive call has own copy of string so separate paths
        #recorded in order visited
        path = path + self.value +","
        print("current path: ", path)
        visited.add(self)
        print("add vertex: ",self.value)
        for adjacent in self.adjacent_vertices:
            if adjacent and adjacent not in visited:
                adjacent.dfs(visited, path)
```

```python
# this version finds a specific value
    def dfs_search(self, searchValue, visited = set(), path = ""):
        path = path + self.value +","
        print("current path: ", path)
        visited.add(self)
        print("add vertex: ",self.value)
        if searchValue == self.value:
            print("Value found")
            return self
        for adjacent in self.adjacent_vertices:
            if adjacent not in visited:
                if adjacent.value == searchValue:
                    print("Value found")
                    path = path + adjacent.value
                    print("current path: ", path)
                    return adjacent
	                vertex_search = adjacent.dfs_search(searchValue, 
		                visited,path)
                
                if vertex_search:
                    return vertex_search
        return None
```

##### [[breadth-first search]]  finds paths horizontally placing each adjacent vertex in a queue and visiting FIFO before descending a level [348]


## Chapter 19:
Topic: 

## Chapter20:

