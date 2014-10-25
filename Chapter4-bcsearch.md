# Chapter 4, beyong classical search

## Heuristic search

Local optimum = highest peak in region
Global optimum = highest mountain in the world

### Hill climbing

* Hill-climbing algorithm
  * Checks if neigbouring solutions have a better value
  * Moves to the best local optimum

* Stochastic hill climbing 
  * Chooses a random move from neigbhouring upphill moves, probability can vary with steepness
  * Genetic algorithms are examples of stochastic hill-climbing   

* Simulated annealing
  * Combination of hill climbing and random walk 
  * Randomnes decrease with time

* Local beam search 
  * Searches several random possistions, chooses the best and starts again.
  *Stops when no better has been found for sertain amount of time.
  
===

* Genetic algorithms
  * Combines diffrent solutions inorder to "breed" a optimal solution
  * Genetic mutations
  * Problem solution must be definable as a set witch can be mixed with other sets
  * Ex vector of numbers  that represent solutions to the problem
  

