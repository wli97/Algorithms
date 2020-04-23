# Classical Search/Optimization Algorithms Memo  
**Data Structures, Algorithm Design, AI**  

### Search Algorithms  
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
      - Uses a heuristic function to expand the most promising node in a greedy way.
      - If h=0 constantly, BF behaves like BFS.
      - Exponential run worst case, linear like DFS if the heurstic is very good.
      - Not optimal, complete if only implemented check-loop.
    - Heuristic:
      - Heuristic uses previous knowledge of the problem to solve exactly one of its relaxed version.
      - Use f=g+h where h is from Best First and g is the cost of path so far. Which combines Uniform and Best.
      - Admissible : Optimistic, h(n) <= d(n).
    - A*:
      - Admissible heuristic search f=max{g+h, fprev}
      - Consistency: as we approach final state, the heuristic cost increasingly approach d(n). So h(n)<=c(n,n+1)+h(n+1).
      - Dominance: h1, h2 both admissible, then if h2>=h1 for all n, h2 dominates h1.
      - Optimal and Complete and Efficient with O(bd) run time if perfect heuristic, often subexponential.
    - Iterative Deepening:
      - DFS with priority based on f cost.
### Optimization
  - Gradient Descent:
    - Find best neighbors, if better than self, move to that point and start again, if not, it is local optimum.
  - Simulated Annealing:
    - Can escape local optimum with probability function that decreases p as # of steps increase (p=e^-(E-Ei)/T).
  - Local Beam Parallel:
    - Does SA with k parallel tasks, and each round keep the best K results to run again.
