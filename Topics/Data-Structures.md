# Data Structures
Data structures are a way of organizing and storing data so that they can be accessed and worked with efficiently. 
They define the relationship between the data, and the operations that can be performed on the data. 
There are several basic and advanced types of data structures, all designed to arrange data to suit a specific purpose. 
All code examples listed here are written in C#.

# Table of Content
- [Arrays](#arrays)
- [Linked Lists](#linked-lists)
- [Stacks](#stacks)
- [Queues](#queues)
- [Hash Tables](#hash-tables)
- [Trees](#trees)
- [Graphs](#graphs)
- [Heap](#heap)
- [Trie](#trie)

## [Arrays](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0)
An array is a series of elements of the same type placed in contiguous memory locations that can be individually referenced by adding an index to a unique identifier.

### Code Example
```
// Declare an array and the size
int[] arr = new int[5]; 
arr[0] = 1; // Assign values to the array  
arr[1] = 2;  
arr[2] = 3;  
arr[3] = 4;  
arr[4] = 5;

// Alternative equivalent approach
int[] arr = new int[5] { 1, 2, 3, 4, 5 };

// Print array length
Console.WriteLine(arr.Length); // Prints: 5

// Access index value
Console.WriteLine(arr[0]); // Prints: 1
```

### Visual Representation
<table>
    <tr>
        <td>1</td>
        <td>2</td>
        <td>3</td>
        <td>4</td>
        <td>5</td>
    </tr>
</table>





## [Linked Lists](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.linkedlist-1?view=net-8.0)
A linked list is a linear data structure where each element is a separate object. Each element (node) of a list consists of two items - the data and a reference to the next node.

### Code Example
```
LinkedList<int> linkedList = new LinkedList<int>(); // Declare a linked list of integers
linkedList.AddLast(6); // Add elements to the end of the linked list
linkedList.AddLast(8);
linkedList.AddLast(2);
linkedList.AddFirst(4); // Add elements at the beginning of the linked list
```

### Visual Representation
![image](https://github.com/XxDaShTixX/Software-Engineering-Interview-Essentials/assets/11358087/bb086a19-7cad-4729-bcff-8e0c5b1c821f)
[Source](https://medium.com/@verdi/working-with-singly-linked-list-928c61ff841e)





## [Stacks](https://learn.microsoft.com/en-us/dotnet/api/system.collections.stack?view=net-8.0)
A stack is a basic LIFO (Last In First Out) data structure that can be logically thought of as a linear structure represented by a real physical stack or pile, a structure where insertion and deletion of items takes place at one end called top of the stack.

### Code Example
```
Stack<char> stack = new Stack<char>(); // Declare a stack
stack.Push('A'); // Push elements onto the stack
stack.Push('B'); // Push ontop of the existing elements
stack.Push('C');
stack.Push('D');
char top = stack.Peek(); // Get the top element: 'D'
char popped = stack.Pop(); // Pop the top element: 'D'
```

### Visual Representation
![image](https://github.com/XxDaShTixX/Software-Engineering-Interview-Essentials/assets/11358087/9fcf9cc9-9c52-4bd1-83aa-930f300d0c0a)  
[Source](https://www.geeksforgeeks.org/how-to-create-a-stack-visualizer-using-html-css-javascript/)





## [Queues](https://learn.microsoft.com/en-us/dotnet/api/system.collections.queue?view=net-8.0)
A queue is a common data structure that places elements in a sequence, similar to a stack. While a stack is LIFO (Last In First Out) data structure, a queue is a FIFO (First In First Out) type.

### Code Example
```
Queue<int> queue = new Queue<int>(); // Declare a queue
queue.Enqueue(2); // Enqueue elements into the queue
queue.Enqueue(3);
queue.Enqueue(4);
queue.Enqueue(5);
queue.Enqueue(6);
queue.Enqueue(7);
queue.Enqueue(8);
queue.Enqueue(9);
int first = queue.Peek(); // Get the first element: 2
int dequeued = queue.Dequeue(); // Dequeue the first element: 2
```

### Visual Representation
![image](https://github.com/XxDaShTixX/Software-Engineering-Interview-Essentials/assets/11358087/bcd2cac9-40de-4888-991c-f3f667011561)  
[Source](https://www.geeksforgeeks.org/difference-between-queue-and-deque-queue-vs-deque/)





## [Hash Tables](https://learn.microsoft.com/en-us/dotnet/api/system.collections.hashtable?view=net-8.0)
A hash table, also known as a hash map, is a data structure that implements an associative array abstract data type, a structure that can map keys to values. 
It uses a hash function to compute an index into an array of buckets or slots, from which the desired value can be found.

### Code Example
```
Hashtable hashtable = new Hashtable(); // Declare a hash table
hashtable.Add("key1", "value1"); // Add key-value pairs to the hash table
hashtable.Add("key2", "value2");
hashtable.Add("key3", "value3");
string value = (string)hashtable["key1"]; // Get the value of a key: "value1"
```

### Visual Representation
<table>
    <tr>
        <th>Key</th>
        <th>Value</th>
    </tr>
    <tr>
        <td>key1</td>
        <td>value1</td>
    </tr>
    <tr>
        <td>key2</td>
        <td>value2</td>
    </tr>
    <tr>
        <td>key3</td>
        <td>value3</td>
    </tr>
</table>





## [Trees](https://www.c-sharpcorner.com/article/tree-data-structure/)
A tree is a widely used abstract data type (ADT) that simulates a hierarchical tree structure, with a root value and subtrees of children with a parent node, represented as a set of linked nodes.

### Code Example
```
public class Node
{
    public char data;
    public Node left;
    public Node right;
    public Node(char data)
    {
        this.data = data;
        left = null;
        right = null;
    }
}

Node root = new Node('A'); // Create a root node
root.left = new Node('B'); // Add left child
root.right = new Node('C'); // Add right child

// Assign left and right leaves to 'B'
Node B = root.left; // Reference B node
B.left = new Node('D'); // Add left child
B.right = new Node('E'); // Add right child

// Assign left and right leaves to 'C'
Node C = root.right; // Reference C node
C.left = new Node('F'); // Add left child
C.right = new Node('G'); // Add right child
```

### Visual Representation
![image](https://github.com/XxDaShTixX/Software-Engineering-Interview-Essentials/assets/11358087/4766f215-a985-47e0-9a7d-ecac5882ed6e)  
[Source](https://pcphunt.blogspot.com/2014/11/trees-in-c.html)





## [Graphs](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2?view=net-8.0)
A graph data structure consists of a finite (and possibly mutable) set of vertices or nodes or points. A direct graph is one with a one-way flow to one Node, not connecting back to itself. Whereas an undirect graph is a two-way flow going from one Node to another and connecting back to itself.

### Code Example for Undirected Graph (two-way stree)
```
Dictionary<int, List<int>> graph = new Dictionary<int, List<int>>();
graph.Add(1, new List<int>() { 2, 3 }); // Add edges between node 1 and nodes 2 and 3
graph.Add(2, new List<int>() { 1, 3, 4, 5 }); // Add edges between node 2 and nodes 1, 3, 4, and 5
graph.Add(3, new List<int>() { 1, 2, 5 }); // Add edges between node 3 and nodes 1, 2, and 5
graph.Add(4, new List<int>() { 2, 5 }); // Add edges between node 4 and nodes 2 and 5
graph.Add(5, new List<int>() { 2, 3, 4 }); // Add edges between node 5 and nodes 2, 3, and 4
```

### Code Example for Directed Graph (one-way street)
```
Dictionary<int, List<int>> graph = new Dictionary<int, List<int>>();
graph.Add(1, new List<int>() { 2, 3 }); // Add directed edges from node 1 to nodes 2 and 3
graph.Add(2, new List<int>() { 3, 4, 5 }); // Add directed edges from node 2 to nodes 3, 4, and 5
graph.Add(3, new List<int>() { 5 }); // Add a directed edge from node 3 to node 5
graph.Add(4, new List<int>() { 5 }); // Add a directed edge from node 4 to node 5
graph.Add(5, new List<int>() { }); // Node 5 has no outgoing edges
```

### Visual Representation
![image](https://github.com/XxDaShTixX/Software-Engineering-Interview-Essentials/assets/11358087/7156c2a9-b656-446d-b114-0f0c6ec9c629)  
[Source](https://learnloner.com/data-structures/graph-data-structure/)




## [Heap](https://www.geeksforgeeks.org/heap-data-structure/)
A Heap is a complete binary tree data structure that satisfies the heap property: for every node, the value of its children is greater than or equal to its own value. Heaps are usually used to implement priority queues, where the smallest (or largest) element is always at the root of the tree.

### Min-Heap
In a min-heap, the root node has the smallest value, and each parent node is less than or equal to its children.

### Max-Heap
In a max-heap, the root node has the largest value, and each parent node is greater than or equal to its children.

### Visual Representation
![image](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20221220165711/MinHeapAndMaxHeap1.png)  
[Source](https://www.geeksforgeeks.org/heap-data-structure/)





## [Trie](https://www.geeksforgeeks.org/introduction-to-trie-data-structure-and-algorithm-tutorials/)
The trie data structure, also known as a prefix tree, is a tree-like data structure used for efficient retrieval of key-value pairs. It is commonly used for implementing dictionaries and autocomplete features, making it a fundamental component in many search algorithms. In this article, we will explore all about Trie data structures in detail.

### Structure
Each node in a trie represents a single character of a string. The root node is associated with an empty string, and each subsequent node represents a character in the key. The path from the root to a node represents the prefix of the key.

### Efficiency
Tries are particularly efficient for operations like prefix searches, autocomplete, and spell checking. They allow for quick retrieval of keys that share common prefixes.

### Insertion and Lookup
To insert a key into a trie, you start from the root and follow the path corresponding to the characters in the key, creating new nodes as needed. For lookup, you traverse the trie following the path of the key’s characters.

### Applications
- **Autocomplete**: Suggesting possible completions for a given prefix.
- **Spell Checking**: Finding words that match a given prefix or correcting misspelled words.
- **Dictionaries**: Efficiently storing and retrieving words and their definitions

### Example
```
public class TrieNode
{
    public TrieNode[] children;
    public int wordCount;
    public TrieNode()
    {
        this.children = new TrieNode[26];
        // This will keep track of number of strings that
        // are stored in the Trie from root node to any Trie
        // node.
        this.wordCount = 0;
    }
}
```

### Visual Representation
![image](https://media.geeksforgeeks.org/wp-content/uploads/20240417114225/trie-data.webp)  
[Source](https://www.geeksforgeeks.org/introduction-to-trie-data-structure-and-algorithm-tutorials/)
