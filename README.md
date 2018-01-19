# Classical Algorithms Memo  
**Data Structures, Algorithm Design, AI**  

- Search Algorithms  
  - Uninformed Search  
    - BFS:  
      - Maintain a closed list of visited nodes (or tag them), and a queue of nodes to visit.
      - Worst Time/Space Complexity = O(b^d) exponential where b=branchs , d=depth of the problem.
      - Complete, and optimal if edges have equal cost.
    - DFS:
      - Importance of searching order.
      - Linear Space Complexity (b^m) where m=max depth of the problem. Same Time Complexity.
      - Incomplete, and might not be optimal if not comparing min. Since it only keeps track of the current path which might encounter infinite loop.  
    - Uniformed:
      - Uses a priority queue with BFS. Works similarly as Dijkstra.
      - Dequeue the edge with minimal/maximal cost.
      - Exponential Complexity but guarantees to find optimal answer for all edges. Also complete.
    - Depth Limited:
      - Impose depth termination. However it is still not complete as solution might exceed imposition.
    - Iterative Deepening:
      - Linear Memory as DFS, Complete as BFS and Optimal if edges equal cost.
      - Explore with increasing depth. This is good if we do not know the solution depth.
      - Very slow to compute.
  - Informed (Heuristic) Search
     - Best First:
     - Heuristic:
     - A*:
