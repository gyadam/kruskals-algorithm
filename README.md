# kruskals-algorithm


[Kruskal's algorithm](https://en.wikipedia.org/wiki/Kruskal%27s_algorithm) is a minimum-spanning-tree algorithm which finds an edge of the least possible weight that connects any two trees in the forest. The repo contains a solution for a minimum-spanning-tree problem with Kruskal in C++, where we read in a distance matrix consisting of distances between villages, and outputs a "map" connecting the villages, i.e. the list of edges from the Kruskal algorithm. 

Before running the Kruskal algorithm, a [disjoint set](https://en.wikipedia.org/wiki/Disjoint-set_data_structure) is created which is the input data structure to the algorithm. [Union by rank](https://en.wikipedia.org/wiki/Disjoint-set_data_structure#Union) and [path compression](https://en.wikipedia.org/wiki/Disjoint-set_data_structure#Path_compression) are used to optimize the algorithm.

![alt text](https://upload.wikimedia.org/wikipedia/commons/b/bb/KruskalDemo.gif)

### Pseudocode of Kruskal's algorithm
```
KRUSKAL(G):
A = ∅
foreach v ∈ G.V:
   MAKE-SET(v)
foreach (u, v) in G.E ordered by weight(u, v), increasing:
   if FIND-SET(u) ≠ FIND-SET(v):   
      A = A ∪ {(u, v)}   
      UNION(FIND-SET(u), FIND-SET(v))   
   return A
```
