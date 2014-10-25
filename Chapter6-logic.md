# Chapter 6, Logical agents

## Knowledge Representation 



What is logic?
A way to make destinctions between good and bad arguments and the tools for making that distinction.

word-list
* Semantics - study of meaning, focus on associating elements of formal language with elements  of a domain of discourse.
  * well-formed formulas = sentences - A word that is part of a formal language
  * proposition - is a sentence expressing if something is true or false
  * Interpretation associates a propositon with an atom
  * atom - simplest well-formed formulas of logic
* Domain of discourse - what sentences can our set of entities be? Ex natural numbers, car colours, natural numbers are all exambles of domains of discourse.

===
### Diffrent types of logic

 Propositional logic:
  * functions: "and" "or" "implies" "not" ""
    * and - w ^ u
    * or  - W v u
    * implication - !W v u
    * not - !w
  * Domain of discourse - propositions about the world
  * atoms - variables
    
### Logic list

& = set of sentences, W = possible worlds, RW = real world
* Syntax
  * Inference - & |-- RW
  * Entailment - & |= W
  
===

## Theorem proving, inference and proofs

* Logical equivalence - two sentences are true in the same sets of models a<=>b
* Validity - A sentence is valid if it's true in all models. a v !a
* satisfiability - a sentence is satisfiable if it's true in some model

## CNF 

How to convert a sentence to CNF form

1. eliminate a <=> b by replacing with (a=>b)^(b=>a)
2. eliminate a=>b by replacing with !a v b
3. CNF requires ! to appear only in litterals so !(!a)=a, !(avb)=(!a)v(!b)
4. We want to distribute v over ^ whenever its possible (a v (b^c)=(avb)^(avc)
