# Chapter 7, Constraint Satisfaction Problem

* Diffrent ways to represent states
   * Atomic - no internal structure, ints - search
   * Factored - vector of internal states, structs - csp
   * Structured - Objects can have relations between othe objects, class - ???
   
===

* What are some constraint satisfaction problems?
  * Map coloring - adjacent squares must have diffrent colors
  * Sudoko
  * Eight queens puzzle
  
* Advantages
  * Representation is closer to the original problem 
  * Algorithms used are domain independent

* How to solve
  * Search - simply tries diffrent solutions and checks if they work
  * Inference - reasoning until solution is found
  * Constraint propogation (cp) - changes possible values in other variables 
  * pre processed by cp then search 
  * cp interleaved with search

===  

Word-list
  * Solution to a CSP - evry variable assigned a value so all constraints are satisfied
  * constraint graph - a graph of all variables and their consistencies
  * Constraints - what type of restriction do the variables have
    * Unary - What can the variable not be - Ex Utah can't be green 
    * Binary - 
    * Higher Order - 
    * Linear - 
    * Nonlinear - 
  * Node consistency - 
  
===
## CSP - Algorithms

Simple Backtracking search
  * Recursive deapth-first search to failure
    * When failing the variable causing it is removed
    * stupid but with inference can lead to intelligent backtracking
  
Intelligent backtracking - heuristic
  * Strategies for choosing variables 
    * Choose the variable with fewest remaining variables - fail early
    * Choose the variable that is involved in the largest number of constraints - hard case first
  
Inference in CSP
* construct constraint graph of problem
* Enforce local consistency in each part of graph 
  * eliminates inconsistent values througout the graph
  * Larger local region -> higher inference cost

