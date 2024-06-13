# Algorithms
Algorithms are a set of instructions that are followed to solve a problem or achieve a particular outcome. 
In the context of computer science and software engineering, algorithms are often used to manipulate data in various structures to produce a specific result. 
They are fundamental to efficient coding and good software design.

# Table of Content
- [Sorting Algorithms](#sorting-algorithms)
  - [Bubble Sort](#bubble-sort)
  - [Selection Sort](#selection-sort)
  - [Insertion Sort](#insertion-sort)
  - [Quick Sort](#quick-sort)
  - [Merge Sort](#merge-sort)
- [Searching Algorithms](#searching-algorithms)
  - [Linear Search](#linear-search)
  - [Jump Search](#jump-search)
  - [Interpolation Search](#interpolation-search)
- [Graph Algorithms](#graph-algorithms)
  - [Depth-First Search (DFS)](#depth-first-search)
  - [Breadth-First Search (BFS)](#breadth-first-search)
  - [Dijkstra's Algorithm](#dijkstras-algorithm)
  - [Bellman-Ford Algorithm](#bellman-ford-algorithm)
- [Dynamic Programming Algorithms](#dynamic-programming-algorithms)
  - [Fibonacci Series](#fibonacci-series)
  - [Knapsack Problem](#knapsack-problem)
  - [Longest Common Subsequence](#longest-common-subsequence)
- [Greedy Algorithms](#greedy-algorithms)
  - [Activity Selection Problem](#activity-selection-problem)
  - [Kruskal's Minimum Spanning Tree (MST)](#kruskals-minimum-spanning-tree)
  - [Huffman Coding](#huffman-coding)

## Sorting Algorithms
These are used to rearrange a given array or list elements according to a comparison operator on the elements.

### Bubble Sort
This is one of the simplest sorting algorithms. It works by repeatedly swapping the adjacent elements if they are in the wrong order. However, it's not suitable for large data sets as its average and worst-case time complexity are both $`O(n^2)`$.

#### Code Example
```
void BubbleSort(int[] arr)
{
    int n = arr.Length;
    for (int i = 0; i < n - 1; i++)
        for (int j = 0; j < n - i - 1; j++)
            if (arr[j] > arr[j + 1])
            {
                // swap arr[j] and arr[j+1]
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
}
```

#### Visual Representation
![image](https://github.com/XxDaShTixX/Software-Engineering-Interview-Essentials/assets/11358087/211d1c1a-71ef-47f1-b272-53537071e14b)  
[Source](https://favtutor.com/blogs/bubble-sort-python)

### Selection Sort
This algorithm sorts an array by repeatedly finding the minimum element from the unsorted part and putting it at the beginning. Like bubble sort, its average and worst-case time complexity are both $`O(n^2)`$, so it's not suitable for large data sets.

#### Code Example
```
void SelectionSort(int[] arr)
{
    int n = arr.Length;
    for (int i = 0; i < n - 1; i++)
    {
        // Find the minimum element in unsorted array
        int min_idx = i;
        for (int j = i + 1; j < n; j++)
            if (arr[j] < arr[min_idx])
                min_idx = j;

        // Swap the found minimum element with the first element
        int temp = arr[min_idx];
        arr[min_idx] = arr[i];
        arr[i] = temp;
    }
}
```

#### Visual Representation
![image](https://github.com/XxDaShTixX/Software-Engineering-Interview-Essentials/assets/11358087/f47f79ee-259b-4fba-91c6-cf187343ec69)  
[Source](https://www.w3resource.com/php-exercises/searching-and-sorting-algorithm/searching-and-sorting-algorithm-exercise-4.php)

### Insertion Sort
This algorithm works by building a sorted array one item at a time. It's much less efficient on large lists than more advanced algorithms like quicksort, heapsort, or merge sort. 
However, insertion sort provides several advantages: simple implementation, efficient for (quite) small data sets, adaptive, stable, and in-place.

#### Code Example
```
void InsertionSort(int[] arr)
{
    int n = arr.Length;
    for (int i = 1; i < n; ++i)
    {
        int key = arr[i];
        int j = i - 1;

        // Move elements of arr[0..i-1], that are greater than key, to one position ahead of their current position
        while (j >= 0 && arr[j] > key)
        {
            arr[j + 1] = arr[j];
            j = j - 1;
        }
        arr[j + 1] = key;
    }
}
```

#### Visual Representation
![image](https://github.com/XxDaShTixX/Software-Engineering-Interview-Essentials/assets/11358087/ab1f268b-44f7-4ef4-a880-200673c1010f)  
[Source](https://www.geeksforgeeks.org/insertion-sort/)

### Quick Sort
This is a highly efficient sorting algorithm and is based on the partitioning of an array of data into smaller arrays. 
A large array is partitioned into two arrays one of which holds values smaller than the specified value, say pivot, based on which the partition is made and another array holds values greater than the pivot value.

#### Code Example
```
int Partition(int[] arr, int low, int high)
{
    int pivot = arr[high];
    int i = (low - 1);
    for (int j = low; j < high; j++)
    {
        if (arr[j] <= pivot)
        {
            i++;
            int temp = arr[i];
            arr[i] = arr[j];
            arr[j] = temp;
        }
    }
    int temp1 = arr[i + 1];
    arr[i + 1] = arr[high];
    arr[high] = temp1;
    return i + 1;
}

void QuickSort(int[] arr, int low, int high)
{
    if (low < high)
    {
        int pi = Partition(arr, low, high);
        QuickSort(arr, low, pi - 1);
        QuickSort(arr, pi + 1, high);
    }
}
```

#### Visual Representation
![image](https://github.com/XxDaShTixX/Software-Engineering-Interview-Essentials/assets/11358087/132fe92c-3590-44b4-bdeb-7135c685e9f0)  
[Source](https://www.enjoyalgorithms.com/blog/quick-sort-algorithm)

### Merge Sort
This is a divide-and-conquer algorithm that divides the input array into two halves, calls itself for the two halves, and then merges the two sorted halves. It's very efficient with time complexity of $`O(n . log(n))`$ in all cases.

#### Code Example
```
void Merge(int[] arr, int l, int m, int r)
{
    int n1 = m - l + 1;
    int n2 = r - m;
    int[] L = new int[n1];
    int[] R = new int[n2];
    for (int a = 0; a < n1; ++a)
        L[a] = arr[l + a];
    for (int b = 0; b < n2; ++b)
        R[b] = arr[m + 1 + b];
    int i = 0, j = 0;
    int k = l;
    while (i < n1 && j < n2)
    {
        if (L[i] <= R[j])
        {
            arr[k] = L[i];
            i++;
        }
        else
        {
            arr[k] = R[j];
            j++;
        }
        k++;
    }
    while (i < n1)
    {
        arr[k] = L[i];
        i++;
        k++;
    }
    while (j < n2)
    {
        arr[k] = R[j];
        j++;
        k++;
    }
}

void MergeSort(int[] arr, int l, int r)
{
    if (l < r)
    {
        int m = l + (r - l) / 2;
        MergeSort(arr, l, m);
        MergeSort(arr, m + 1, r);
        Merge(arr, l, m, r);
    }
}
```

#### Visual Representation
![image](https://github.com/XxDaShTixX/Software-Engineering-Interview-Essentials/assets/11358087/50979a86-76b3-4c70-bd26-45c8d6d17bbb)  
[Source](https://medium.com/@ozgurmehmetakif/merge-sort-algorithm-ff52822f5608)



## Searching Algorithms
Searching algorithms are used to locate specific items within a collection of data based on certain search criteria.

### Linear Search
This is the simplest type of search algorithm. It works by sequentially checking each element in the list until it finds an element that matches the target value. 
If the algorithm reaches the end of the list, the search terminates unsuccessfully.

#### Code Example
```
int LinearSearch(int[] arr, int x)
{
    int n = arr.Length;
    for (int i = 0; i < n; i++)
        if (arr[i] == x)
            return i;
    return -1;
}
```

#### Visual Representation
![image](https://www.tutorialspoint.com/data_structures_algorithms/images/linear_search.gif)  
[Source](https://www.tutorialspoint.com/data_structures_algorithms/linear_search_algorithm.htm)

### Jump Search
Like Binary Search, Jump Search is a searching algorithm for sorted arrays. The basic idea is to check fewer elements (than linear search) by jumping ahead by fixed steps or skipping some elements in place of searching all elements.

#### Code Example
```
int JumpSearch(int[] arr, int x)
{
    int n = arr.Length;
    int step = (int)Math.Floor(Math.Sqrt(n));
    int prev = 0;
    while (arr[Math.Min(step, n) - 1] < x)
    {
        prev = step;
        step += (int)Math.Floor(Math.Sqrt(n));
        if (prev >= n)
            return -1;
    }
    while (arr[prev] < x)
    {
        prev++;
        if (prev == Math.Min(step, n))
            return -1;
    }
    if (arr[prev] == x)
        return prev;
    return -1;
}
```

#### Visual Representation
![image](https://harkishen-singh.github.io/jump-search-visualisation/this.gif)  
[Source](https://harkishen-singh.github.io/jump-search-visualisation/)

### Interpolation Search
The Interpolation Search is an improvement over Binary Search for instances, where the values in a sorted array are uniformly distributed. 
Binary Search always goes to the middle element to check. On the other hand, interpolation search may go to different locations according to the value of the key being searched.

#### Code Example
```
int InterpolationSearch(int[] arr, int x)
{
    int lo = 0, hi = (arr.Length - 1);
    while (lo <= hi && x >= arr[lo] && x <= arr[hi])
    {
        if (lo == hi)
        {
            if (arr[lo] == x) return lo;
            return -1;
        }
        int pos = lo + (((hi - lo) / (arr[hi] - arr[lo])) * (x - arr[lo]));
        if (arr[pos] == x)
            return pos;
        if (arr[pos] < x)
            lo = pos + 1;
        else
            hi = pos - 1;
    }
    return -1;
}
```

#### Visual Representation
![image](https://upload.wikimedia.org/wikipedia/commons/0/08/Interpolation_sort.gif)  
[Source](https://commons.wikimedia.org/wiki/File:Interpolation_sort.gif)



## Graph Algorithms
Graph algorithms are methods used to traverse and analyze graphs, solving various problems such as finding a specific node or the path between two given nodes.

### Depth-First Search (DFS)
This algorithm explores as far as possible along each branch before backtracking. It uses a stack as its underlying data structure.

#### Code Example
```
void DFS(int v, bool[] visited, List<int>[] adj)
{
    visited[v] = true;
    foreach (var node in adj[v])
    {
        if (!visited[node])
            DFS(node, visited, adj);
    }
}
```

#### Visual Representation
![image](https://upload.wikimedia.org/wikipedia/commons/7/7f/Depth-First-Search.gif)  
[Source](https://commons.wikimedia.org/wiki/File:Depth-First-Search.gif)

### Breadth-First Search (BFS)
This algorithm explores all the vertices of a graph in breadth-first order. It uses a queue as its underlying data structure.

#### Code Example
```
void BFS(int v, bool[] visited, List<int>[] adj)
{
    Queue<int> queue = new Queue<int>();
    visited[v] = true;
    queue.Enqueue(v);
    while (queue.Count != 0)
    {
        v = queue.Dequeue();
        foreach (var node in adj[v])
        {
            if (!visited[node])
            {
                queue.Enqueue(node);
                visited[node] = true;
            }
        }
    }
}
```

#### Visual Representation
![image](https://upload.wikimedia.org/wikipedia/commons/5/5d/Breadth-First-Search-Algorithm.gif)  
[Source](https://commons.wikimedia.org/wiki/File:Breadth-First-Search-Algorithm.gif)

### Dijkstra's Algorithm
This is a shortest path algorithm for a graph with non-negative edge path costs, producing a shortest path tree.

#### Code Example
```
void Dijkstra(int[,] graph, int src, int V)
{
    int[] dist = new int[V];
    bool[] sptSet = new bool[V];
    for (int i = 0; i < V; i++)
    {
        dist[i] = int.MaxValue;
        sptSet[i] = false;
    }
    dist[src] = 0;
    for (int count = 0; count < V - 1; count++)
    {
        int u = MinDistance(dist, sptSet, V);
        sptSet[u] = true;
        for (int v = 0; v < V; v++)
            if (!sptSet[v] && Convert.ToBoolean(graph[u, v]) && dist[u] != int.MaxValue && dist[u] + graph[u, v] < dist[v])
                dist[v] = dist[u] + graph[u, v];
    }
}
```

#### Visual Representation
![image](https://upload.wikimedia.org/wikipedia/commons/5/57/Dijkstra_Animation.gif)  
[Source](https://commons.wikimedia.org/wiki/File:Dijkstra_Animation.gif)

### Bellman-Ford Algorithm
This algorithm computes shortest paths from a single source vertex to all of the other vertices in a weighted digraph. 
It is slower than Dijkstra’s algorithm for the same problem, but more versatile, as it is capable of handling graphs in which some of the edge weights are negative numbers.

#### Code Example
```
void BellmanFord(int[,] graph, int src, int V, int E)
{
    int[] dist = new int[V];
    for (int i = 0; i < V; i++)
        dist[i] = int.MaxValue;
    dist[src] = 0;
    for (int i = 0; i < V - 1; i++)
        for (int j = 0; j < E; j++)
            if (dist[graph[j, 0]] != int.MaxValue && dist[graph[j, 0]] + graph[j, 2] < dist[graph[j, 1]])
                dist[graph[j, 1]] = dist[graph[j, 0]] + graph[j, 2];
}
```

#### Visual Representation
![image](https://upload.wikimedia.org/wikipedia/commons/7/77/Bellman%E2%80%93Ford_algorithm_example.gif)  
[Source](https://commons.wikimedia.org/wiki/File:Bellman%E2%80%93Ford_algorithm_example.gif)



## Dynamic Programming Algorithms
Dynamic Programming algorithms are methods used to solve complex problems by breaking them down into simpler subproblems. These algorithms store the solutions of these subproblems to avoid redundant computations, leading to more efficient solutions.

### Fibonacci Series
The Fibonacci sequence is a series of numbers where a number is the addition of the last two numbers. The dynamic programming approach to calculate the Fibonacci series results in an $`O(n)`$ time complexity.

#### Code Example
```
int Fibonacci(int n)
{
    int[] f = new int[n + 2];
    f[0] = 0;
    f[1] = 1;
    for (int i = 2; i <= n; i++)
        f[i] = f[i - 1] + f[i - 2];
    return f[n];
}
```

### Knapsack Problem
The knapsack problem is a problem in combinatorial optimization: 
Given a set of items, each with a weight and a value, determine the number of each item to include in a collection so that the total weight is less than or equal to a given limit and the total value is as large as possible.

#### Code Example
```
int Knapsack(int W, int[] wt, int[] val, int n)
{
    int[,] K = new int[n + 1, W + 1];
    for (int i = 0; i <= n; i++)
    {
        for (int w = 0; w <= W; w++)
        {
            if (i == 0 || w == 0)
                K[i, w] = 0;
            else if (wt[i - 1] <= w)
                K[i, w] = Math.Max(val[i - 1] + K[i - 1, w - wt[i - 1]], K[i - 1, w]);
            else
                K[i, w] = K[i - 1, w];
        }
    }
    return K[n, W];
}
```

### Longest Common Subsequence
Given two sequences, find the length of the longest subsequence present in both of them. A subsequence is a sequence that appears in the same relative order, but not necessarily contiguous.

#### Code Example
```
int LCS(string X, string Y, int m, int n)
{
    int[,] L = new int[m + 1, n + 1];
    for (int i = 0; i <= m; i++)
    {
        for (int j = 0; j <= n; j++)
        {
            if (i == 0 || j == 0)
                L[i, j] = 0;
            else if (X[i - 1] == Y[j - 1])
                L[i, j] = L[i - 1, j - 1] + 1;
            else
                L[i, j] = Math.Max(L[i - 1, j], L[i, j - 1]);
        }
    }
    return L[m, n];
}
```



## Greedy Algorithms
Greedy algorithms are methods that make locally optimal choices at each step with the hope of finding a global optimum. These algorithms make decisions based on the current information without considering the future consequences.

### Activity Selection Problem
The problem is to select the maximum number of activities that can be performed by a single person or machine, assuming that a person can only work on a single activity at a time.

#### Code Example
```
public class Activity
{
    public int start, finish;
    public Activity(int start, int finish)
    {
        this.start = start;
        this.finish = finish;
    }
}

public class ActivityComparer : IComparer<Activity>
{
    public int Compare(Activity x, Activity y)
    {
        return x.finish.CompareTo(y.finish);
    }
}

public void PrintMaxActivities(Activity[] arr, int n)
{
    Array.Sort(arr, new ActivityComparer());
    int i = 0;
    for (int j = 1; j < n; j++)
    {
        if (arr[j].start >= arr[i].finish)
        {
            i = j;
        }
    }
}
```

### Kruskal's Minimum Spanning Tree (MST)
This algorithm is a minimum-spanning-tree algorithm which finds an edge of the least possible weight that connects any two trees in the forest.

#### Code Example
```
class Edge
{
    public int src, dest, weight;
}

class Subset
{
    public int parent, rank;
}

int find(Subset[] subsets, int i)
{
    if (subsets[i].parent != i)
        subsets[i].parent = find(subsets, subsets[i].parent);
    return subsets[i].parent;
}

void Union(Subset[] subsets, int x, int y)
{
    int xroot = find(subsets, x);
    int yroot = find(subsets, y);
    if (subsets[xroot].rank < subsets[yroot].rank)
        subsets[xroot].parent = yroot;
    else if (subsets[xroot].rank > subsets[yroot].rank)
        subsets[yroot].parent = xroot;
    else
    {
        subsets[yroot].parent = xroot;
        subsets[xroot].rank++;
    }
}

void KruskalMST(Graph graph)
{
    int V = graph.V;
    Edge[] result = new Edge[V];
    int e = 0;
    int i = 0;
    for (i = 0; i < V; ++i)
        result[i] = new Edge();
    Array.Sort(graph.edge);
    Subset[] subsets = new Subset[V];
    for (i = 0; i < V; ++i)
        subsets[i] = new Subset();
    for (int v = 0; v < V; ++v)
    {
        subsets[v].parent = v;
        subsets[v].rank = 0;
    }
    i = 0;
    while (e < V - 1)
    {
        Edge next_edge = graph.edge[i++];
        int x = find(subsets, next_edge.src);
        int y = find(subsets, next_edge.dest);
        if (x != y)
        {
            result[e++] = next_edge;
            Union(subsets, x, y);
        }
    }
}
```

### Huffman Coding
Huffman coding is a lossless data compression algorithm. The idea is to assign variable-length codes to input characters, lengths of the assigned codes are based on the frequencies of corresponding characters.

#### Code Example
```
public class MinHeapNode
{
    public char data;
    public int freq;
    public MinHeapNode left, right;
    public MinHeapNode(char data, int freq)
    {
        this.data = data;
        this.freq = freq;
        left = right = null;
    }
}

void printCodes(MinHeapNode root, string str)
{
    if (root == null)
        return;
    if (root.data != '$')
        Console.WriteLine(root.data + ": " + str);
    printCodes(root.left, str + "0");
    printCodes(root.right, str + "1");
}

void Huffman(char[] charArray, int[] charfreq, int n)
{
    MinHeapNode left, right, top;
    for (int i = 0; i < n; i++)
        minHeap.insert(new MinHeapNode(charArray[i], charfreq[i]));
    while (!minHeap.isEmpty())
    {
        left = minHeap.extractMin();
        right = minHeap.extractMin();
        top = new MinHeapNode('$', left.freq + right.freq);
        top.left = left;
        top.right = right;
        minHeap.insert(top);
    }
    printCodes(minHeap.extractMin(), "");
}
```
