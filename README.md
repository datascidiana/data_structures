# Implementations of data structures in python
In this repository are my implementations of the following data structures:
1. Doubly Linked List
2. Circular Queue
3. Stack
4. Hash Table
5. BS Tree / AVL Tree
6. Heap / Priority Queue

## Linked List
A doubly linked list is a sequential data structure of unordered linked elements known as nodes. It is represented by the first sentinel node, called head, which keep track of start and end of the list. Each node consists of value (data) and references to next and previous nodes.
* Avantages: dynamic size, constant time insertion/deletion at front/end;
* Drawbacks: random access not allowed (sequencial access), extra memory space for references.

Time complexity:
* access: O(n)
* search: O(n)
* insertion: O(1)
* deletion: O(1)

## Circular Queue
Circular Queue is a linear data structure in which the operations are performed based on FIFO(First In First Out) principle and the last position is connected back to the first position to make a circle. Circular queue performs the following opperations: enqueue - adds an item at the end(tail), dequeue - removes the first item(head).
* Avantages: manage data in a particular way (FIFO), constant time insertion and deletion;
* Drawbacks: no random access.

Time complexity:
* access: O(n)
* search: O(n)
* insertion: O(1)
* deletion: O(1)

Implementation:
The queue is represented by an array, tail, head, and count. The head and tail keep track of their position in array, and count keeps track of the number of elements in the queue. To add a new value to the queue, we enqueue, which means promoting tail's position to the next position available in the array/queue and storing the value. To delete a value, we dequeue, which means promoting head's position by one and deleting the previous value for the head. To resize the array for the queue, we are inserting new cells at the head's position.

## Stack
Stack is a linear data structure which follows a particular order in which the operations are performed: LIFO(Last In First Out) or FILO(First In Last Out). Stack performs the following opperations: push - adds an item in the stack, pop - removes an item from the stack in the reversed order in which they are pushed, peek - returns top element of stack, empty - returns true if its empty and false otherwise.
* Avantages: manage data in a particular way (LIFO/FILO), constant time insertion and deletion;
* Drawbacks: no random access.

Time complexity:
* access: O(n)
* search: O(n)
* insertion: O(1)
* deletion: O(1)

Implementation:
Stack consists of nodes, reference to the next node, and a top node. To push a node, we add a node before the top node, which makes the new one - top node. To pop a node, we return the value of the top node and promote next node as top node.

## Hash Table
Hash Table is a data structure which stores data in an associative manner. In a hash table, data is stored in an array format, where each data value has its own unique index value, obtained through hashing, which is is a technique to convert a range of key values into a range of indexes of an array. Access of data becomes very fast if we know the index of the desired data. Thus, it becomes a data structure in which insertion and search operations are very fast irrespective of the size of the data. However, worst case scenario - hash collisions for all items, makes search, insertion and deletion operations too slow, O(n).
* Avantages: constant time search, insertion and deletion;
* Drawbacks: hash collisions.

Time complexity:
* search: O(1)
* insertion: O(1)
* deletion: O(1)

Implementation:
It has 2 arrays: indices - stores indices of the spot in the entries array for the key and value pairs and forms linked lists of indices, in case of collisions, entries - stores key and value pairs. For each key and value pair, the key is hashed, the hash value is the index in the indices array where the index of the next cell in the entries array is stored, then the key and value pair is appended to the entries array.

## BS Tree / AVL Tree
Binary Search Tree is a node-based binary tree data structure, where the left subtree has values lesser than the parent node's key and the right subtree - larger. AVL Tree is a similar data structure, the difference is that it is self-balancing, which means that the difference between the heights of the left and right subtrees cannot be more than one.

Time complexity:
* access: O(log(n))
* search: O(log(n))
* insertion: O(log(n))
* deletion: O(log(n))

Implementation:
The Binary Search Tree contains nodes, which have a key, value, and references to the right and left nodes. It also has size and root node. To add a value, we use the "setitem" reserved method, and inside it we have another recursive method, that iterates through the tree, comparing the key to the parent key, choosing right or left path accordingly. When there's no more nodes left to iterate, a new one is added with the repsective key and value and the size is incremented by one. To search for a key, same strategy is used. To delete an item we traverse it the way we do for setitem and getitem. When we find the node we want to delete, if there's no subtrees, we just return None in node's place, if there's only one subtree - right or left, then we return that subtree in node's place. In case there's two subtrees, we move on to the left node, and if it doesn't have a right subtree, it is promoted in the place of the deleted node. Otherwise, we traverse through the right subtrees, until there's no more. Then, we promote the left subtree up instead of the last node on the right, and replace the key and value of the node to be deleted with the left subtree's node.
The AVL Tree containes nodes with a value and references to the right and left subtree as well, but the Node class also has methods to rotate the tree left or right and a height method. To rotate, we first replace parent node's value with its left/right child dependeing on the direction of the rotation, and then change references in such a way that it would still obey AVL Tree's properties.

## Heap / Priority Queue

A heap is a tree-based data structure in which all the nodes of the tree are in a specific order. For example, in a max heap, parent's value is always larger than its children. 

Time complexity:
* access: O(log(n))
* search: O(log(n))
* insertion: O(log(n))
* deletion: O(log(n))
* min/max: O(1)

Implementation:
Heap consists of an array and a key function that decides how to prioritize nodes. It has functions that calculate the index of the parent, left and right child nodes, using simple formulas. In the add function, the value is appended to the array, then checks if the parent node's value is lesser than the new value added, and swaps them. It keeps checking and swapping the node and its parent node until runs out of nodes to check. To pop a value, we retrun first value in the array, replace it with the last value, and then heapify. To heapify, we compare the value of the node to its left and right child, then swap if necessary, and repeat until no swaps are needed.


