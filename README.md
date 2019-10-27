### Implementations of data structures in python
In this repository are my implementations of the following data structures:
1. Doubly Linked List
2. Circular Queue
3. Stack
4. Hash Table
5. BS Tree / AVL Tree
6. Heap

# Linked List
A doubly linked list is a sequential data structure of unordered linked elements known as nodes. It is represented by the first sentinel node, called head, which keep track of start and end of the list. Each node consists of value (data) and references to next and previous nodes.
Avantages: dynamic size, constant time insertion/deletion at front/end;
Drawbacks: random access not allowed (sequencial access), extra memory space for references.
Time complexity:
access: O(n)
search: O(n)
insertion: O(1)
deletion: O(1)

# Circular Queue
Circular Queue is a linear data structure in which the operations are performed based on FIFO(First In First Out) principle and the last position is connected back to the first position to make a circle. Circular queue performs the following opperations: enqueue - adds an item at the end(tail), dequeue - removes the first item(head).
Avantages: manage data in a particular way (FIFO), constant time insertion and deletion;
Drawbacks: no random access.
Time complexity:
access: O(n)
search: O(n)
insertion: O(1)
deletion: O(1)

# Stack
Stack is a linear data structure which follows a particular order in which the operations are performed: LIFO(Last In First Out) or FILO(First In Last Out). Stack performs the following opperations: push - adds an item in the stack, pop - removes an item from the stack in the reversed order in which they are pushed, peek - returns top element of stack, empty - returns true if its empty and false otherwise.
Avantages: manage data in a particular way (LIFO/FILO), constant time insertion and deletion;
Drawbacks: no random access.
Time complexity:
access: O(n)
search: O(n)
insertion: O(1)
deletion: O(1)

# Hash Table
Hash Table is a data structure which stores data in an associative manner. In a hash table, data is stored in an array format, where each data value has its own unique index value, obtained through hashing, which is is a technique to convert a range of key values into a range of indexes of an array. Access of data becomes very fast if we know the index of the desired data. Thus, it becomes a data structure in which insertion and search operations are very fast irrespective of the size of the data. However, worst case scenario - hash collisions for all items, makes search, insertion and deletion operations too slow, O(n).
Avantages: constant time search, insertion and deletion;
Drawbacks: hash collisions.
Time complexity:
search: O(1)
insertion: O(1)
deletion: O(1)

Implementation:
It has 2 arrays: indices - stores indices of the key and value pairs in the entries array and forms linked lists in case of collisions, entries - stores key and value pairs. For each key and value pair, the key is hashed, the hash value is the index in the indices array where the index of the next cell in the entries array is stored, then the key and value pair is appended to the entries array.

# BS Tree / AVL Tree
Binary Search Tree is a node-based binary tree data structure, where the left subtree has values lesser than the parent node's key and the right subtree - larger.

Time complexity:
access: O(log(n))
search: O(log(n))
insertion: O(log(n))
deletion: O(log(n))


# Heap


