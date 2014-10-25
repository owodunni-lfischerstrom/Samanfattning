# Chapter 5, adverserial search

* Multi-Agent enviroments
* Game must be evaluable by some function
* Agents try to maximize there score while minimizing oponents score
* Search till game ends



## Minmax search
Perfect for two player games like chess

* Minmax algorithm
  * Generate complete game tree using deapth-first search
  * Evaluate game states using some utility function
  * From root max chooses the move that leads to the highes value

===

* Alpha-beta pruning
  * Layerd on top of minmax
  * Searches with deepth first to give alpha and beta some values
  * Any part of the tree that gives worse values gets pruned
  * Alpha = best value of an already explored path for the maximizer
  * Beta = best value of an already explored path for the minimizer
  
 * When to prune? 
  * A maximzer node will prune if its current value is higher then beta
  * A minimizer will prune if its current value is lower than alpha
  





