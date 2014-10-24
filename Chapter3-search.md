#Chapter 3, search

* word-list Search
 * States - states in the state space
 * parent node - predecending nodes
 * Action - generates nodes in a search tree or movement in the state space
 * Depth - Nodes from root to current node
 * Path cost - cost between two nodes in a search tree
 * Frontier - nodes to be expanded
 * admissible - heuristic function never overestimate cost

===
 
* A strategy is defined by the order of node expansion
 * completness - does the strategy find a solution if one exists?
 * Time complexity - numb nodes expandes
 * Space complexity - maximum number of nodes in memory
 * Optimality - does the strategy find the optimal solution?

===

*Graph vs Tree search
 * Graph search keeps track of visited nodes ex - explored hash table
 * Tree search does not keep track and is suseptible for infinity loop

===
## Problem definition

* Five cpmponents to formally define problems
 * Initial state
 * Possible actions
 * Transition model, what does the actions do
 * Goal test
 * A path cost

===

## Uniformed search algorithms
Uniformed search = Blind search
b = branching factor
d = deepth from root
m = max deepth
e = min path cost
c*= optimal cost
l = deepth limit


* Breath-First search
 * New nodes added to back of frontier
 * Nodes goal tested when added to frontier
 * Complet - yes
 * Optimal when cost are uniform
 * Time O(b^d)
 * Space O(b^d)

===

* Deep first search 
 * New nodes get added to the front of the frontier 
 * Complet - in graph search if the state space is finite
 * Optimal - no
 * Time O(b^m)
 * Space O(b*m) with backtracking O(m)
 
 
===

* Uniformed cost
 * Expandes the node with the lowest path cost from the node 
 * A priority queue on path cost is used instead of a FIFO queue
 * complete - yes
 * optimal - yes
 * Time - O(b^(1+C*/e))
 * Complexity - O(b^(1+C*/e))

===

* Iterative deepening
 * Deep-first search to l, if goal not found, goal search l=l+1
 * Complete - yes if finite
 * Optimal - yes if path cost is uniform
 * Time O(b^d)
 * Complexity O(bd)
 
===

* Bidirectional
 * Searches from goal and start simultanius
 * Compares searched nodes to find if the searchspaces intersect
 * Complete - Depends on algorithm
 * Optimal - Depends on algorithm
 * Time and space are cut in half
 
===

## Informed search
f(n) = function used by algorith to evaluate new nodes

* Greedy best-first search
 * f(n)=g(n)
 * g(n) admissible heuristic to estimate distance to goal
 * Complete - yes in graph search in finite state space
 * Optimal - no
 
* A*
 * f(n) = g(n) + h(n)
 * g(n) admissible heuristic to estimate distance to goal
 * h(n) cost from root to node
 * Complete - yes se below
 * Optimal yes se below
 
### A* - proof of optimality

* A* is optimal in tree-search if f(n) is admissible
* A* is optimal in graph-search if h(n) is consistent
 * h(n) being consistent means that the distance from root to leaf is always increasing with deepth.
 * c(n,a,n') cost from n to n' while preforming action a

Proof:
g(n') = g(n)  + c(n,a,n')
f(n') = g(n') + h(n') = g(n) + c(n,a,n') + h(n') >= g(n) + h(n) = f(n)

The cost will always increase while we move deeper in a consistent search-tree.
When A* expandes a node that means that the optimal path to that node from the root.

* A* expandes all nodes with f(n) < goal cost
* A* might then expand some node right on the "goal contour" where f(n) = goal cost
* Completness requires finite amount of nodes with cost < goal cost
* A* is optimally efficient

===
 
 ### Inventing Admissible heuristics
 
 * The cost of an optimal solution to a relaxed problem is in fact





  
