
## Basic Syntactic Mutation

Basic Syntactic Mutation (BSM) is a mutation based unification algorithm for the theories that are saturated by paramodulation. The algorithm has been introduced by Christopher Lynch *et al.* in the paper [Basic Syntactic Mutation](http://people.clarkson.edu/~clynch/PAPERS/bsm.ps).

Inspired by the above work, we developed a new and simplified mutation-based unification algorithm for solving a unification problem modulo the theories that are both convergent and forward closed.
We call the algorithm as **BSM'**.
The BSM' procedure consists of inference rules such as **Coalesce**, **Split**, **Imit**, **MutConflict**, and **ImitCycle**. The inference procedure prioritize the rules in the following order: *Coalesce*, *Split*, and then applies the rules *Imit*, *MuConflict*, and *ImitCycle* in a non-deterministic way.
We have implemented the procedure in [Maude](http://maude.cs.illinois.edu/), a high performance reflective language.

For more details about the BSM' procedure, please see the following paper.
* Ajay K. Eeralla, Serdar Erbatur, Andrew M. Marshall, Christophe Ringeissen. [Unification in Non-Disjoint Combinations with Forward-Closed Theories (extended version)](http://members.loria.fr/CRingeissen/files/papers/combi-fc.pdf).


## Prerequisites 
To run the algorithm you will need to have installed Maude. 

### Install 
Download and install Maude from [here](http://maude.cs.illinois.edu/w/index.php?title=The_Maude_System).

### Instructions to run the program 

Download .maude file(s) to a directory. Then navigate to the directory and run the following commands.

1. #### Load the file using the following command 

 ``` 
 > load filename.maude 
 ```

2. #### Testing 

 ```
 > red in myBSMPrime : bsmUnify ( UnPr , RWS, BAL, N, SUB ) 
 ```
 
 where `UnPr` is an unification problem, `RWS` is a rewrite system, `BAL` is a data structure that keeps tracking the box-status of the terms (`Empty` at the begining), `N` is a new-variable-counter (`0` initially), and `SUB` is the substitution or solution. Of course, `SUB` is `none` at the begining.

<!---## Tested Results --->

<!---Unification Problem | Rewrite System | Solution | Real Time (ms)
------------ | ------------- | ------------- | ------------- 
`'f['x:Nat , 'y:Nat]  =? 'y:Nat`| `emptyrs` | `fail` | `0` --->

3. ## Publications

* Ajay K. Eeralla, Serdar Erbatur, Andrew M. Marshall, Christophe Ringeissen. [Rule-Based Unification in Combined Theories and the Finite Variant Property](https://link.springer.com/chapter/10.1007/978-3-030-13435-8_26)in Language and Automata Theory and Applications - 13th International Conference, LATA 2019, St. Petersburg, Russia, March 26-29, 2019, Proceedings.

<!---## Authors
* Ajay Kumar Eeralla, University of Missouri-Columbia (USA)
* Serdar Erbatur, Ludwig-Maximilians-Universitat Munchen (Germany)
* Andrew M. Marshall, University of Mary Washington (USA)
* Christophe Ringeissen, Universite de Lorraine, CNRS, Inria, LORIA (France)--->

