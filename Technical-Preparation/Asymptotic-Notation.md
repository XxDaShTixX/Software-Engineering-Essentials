# Asymptotic Notation
A mathematical notation used in computer science to describe the efficiency of algorithms. 
It gives an upper or lower bound on the growth rate of a function, such as the time complexity of an algorithm. 
The most common types are Big O (O), which represents the upper bound, and Omega (Ω), which represents the lower bound.

## Complexities
Here are some common time complexities or rates of growth for algorithms, listed from best to worst:

- Constant Time: $`O(1)`$ - The running time of the algorithm is constant and does not depend on the size of the input.
- Logarithmic Time: $`O(log(n))`$ - The running time of the algorithm increases logarithmically with the size of the input.
- Linear Time: $`O(n)`$ - The running time of the algorithm increases linearly with the size of the input.
- Linear Logarithmic Time: $`O(n . log(n))`$ - The running time of the algorithm increases linearly and logarithmically with the size of the input.
- Quadratic Time: $`O(n^2)`$ - The running time of the algorithm increases quadratically with the size of the input.
- Cubic Time: $`O(n^3)`$ - The running time of the algorithm increases cubically with the size of the input.
- Exponential Time: $`O(2^n)`$ - The running time of the algorithm doubles with each addition to the input data set.
- Factorial Time: $`O(n!)`$ - The running time of the algorithm grows factorial with the size of the input.

![image](https://github.com/XxDaShTixX/Software-Engineering-Interview-Essentials/assets/11358087/fd836a36-bbfe-474f-9628-c8791a020d53)  
[Source](https://en.wikipedia.org/wiki/Computational_complexity_of_mathematical_operations)

## Complexity Analysis
This table provides a comparative analysis of the time complexities for various operations (indexing, search, insertion, and optimized search) across different data structures and algorithms. 
It serves as a quick reference guide for understanding the efficiency of these operations, thereby aiding in the selection of appropriate data structures and algorithms for specific programming tasks.  

<table role=“table”>
   <thead>
      <tr>
         <th>No.</th>
         <th>Name</th>
         <th>Indexing</th>
         <th>Search</th>
         <th>Insertion</th>
         <th>Optimized Search</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td>1</td>
         <td>Linear Array</td>
         <td>O(1)</td>
         <td>O(n)</td>
         <td>N/A</td>
         <td>O(log n)</td>
      </tr>
      <tr>
         <td>2</td>
         <td>Dynamic Array</td>
         <td>O(1)</td>
         <td>O(n)</td>
         <td>O(n)</td>
         <td>O(log n)</td>
      </tr>
      <tr>
         <td>3</td>
         <td>Linked List</td>
         <td>O(n)</td>
         <td>O(n)</td>
         <td>O(1)</td>
         <td>O(n)</td>
      </tr>
      <tr>
         <td>4</td>
         <td>Hash Table</td>
         <td>O(1)</td>
         <td>O(1)</td>
         <td>O(1)</td>
         <td> </td>
      </tr>
      <tr>
         <td>5</td>
         <td>Binary Tree</td>
         <td>O(log n)</td>
         <td>O(log n)</td>
         <td>O(log n)</td>
         <td> </td>
      </tr>
      <tr>
         <td>6</td>
         <td>Breadth First Search</td>
         <td> </td>
         <td>O(|E| + |V|) E: # of edges V: # of vertices</td>
         <td> </td>
         <td> </td>
      </tr>
      <tr>
         <td>7</td>
         <td>Depth First Search</td>
         <td> </td>
         <td>O(|E| + |V|) E: # of edges V: # of vertices</td>
         <td> </td>
         <td> </td>
      </tr>
      <tr>
         <td>8</td>
         <td>Stack</td>
         <td>O(1)</td>
         <td>O(n)</td>
         <td>O(1)</td>
         <td>N/A</td>
      </tr>
      <tr>
         <td>9</td>
         <td>Queue</td>
         <td>O(1)</td>
         <td>O(n)</td>
         <td>O(1)</td>
         <td>N/A</td>
      </tr>
      <tr>
         <td>10</td>
         <td>Heap</td>
         <td>N/A</td>
         <td>O(n)</td>
         <td>O(log n)</td>
         <td>O(1)</td>
      </tr>
      <tr>
         <td>11</td>
         <td>Binary Search Tree</td>
         <td>N/A</td>
         <td>O(log n)</td>
         <td>O(log n)</td>
         <td>O(log n)</td>
      </tr>
      <tr>
         <td>12</td>
         <td>Red-Black Tree</td>
         <td>N/A</td>
         <td>O(log n)</td>
         <td>O(log n)</td>
         <td>O(log n)</td>
      </tr>
      <tr>
         <td>13</td>
         <td>Hash Map</td>
         <td>O(1)</td>
         <td>O(1)</td>
         <td>O(1)</td>
         <td>O(1)</td>
      </tr>
      <tr>
         <td>14</td>
         <td>Graph (Adjacency List)</td>
         <td>O(|V|)</td>
         <td>O(|V|)</td>
         <td>O(1)</td>
         <td>O(|V|)</td>
      </tr>
      <tr>
         <td>15</td>
         <td>Graph (Adjacency Matrix)</td>
         <td>O(1)</td>
         <td>O(|V|^2)</td>
         <td>O(1)</td>
         <td>O(|V|^2)</td>
      </tr>
      <tr>
         <td>16</td>
         <td>Dijkstra’s Algorithm</td>
         <td>N/A</td>
         <td>O((|V|+|E|) log |V|)</td>
         <td>N/A</td>
         <td>N/A</td>
      </tr>
      <tr>
         <td>17</td>
         <td>Bellman-Ford Algorithm</td>
         <td>N/A</td>
         <td>O(|V|*|E|)</td>
         <td>N/A</td>
         <td>N/A</td>
      </tr>
   </tbody>
</table>  
  
**Indexing**: This column shows the time complexity of accessing an element at a particular index in the data structure. 
For example, accessing an element in an array by its index is a constant time operation, denoted as $`O(1)`$.  

**Search**: This column represents the time complexity of searching for an element in the data structure. 
The exact time complexity can vary depending on the data structure and the specific search algorithm used.  

**Insertion**: This column indicates the time complexity of inserting a new element into the data structure. 
Again, this can vary widely depending on the data structure.  

**Optimized Search**: This column represents the time complexity of the most efficient search operation possible for the data structure, assuming certain conditions are met. 
For example, binary search on a sorted array has a time complexity of O(log n), which is more efficient than a linear search with a time complexity of $`O(n)`$.
