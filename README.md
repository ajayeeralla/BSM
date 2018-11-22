
## Basic Syntactic Mutation (BSM)

Basic syntactic mutation prime is a new mutation based unification algorithm
for theories defined by rewrite systems which are both convergent and
forward-closed. The algorithm is well suited for combination. The BSM procedure consists of inference rules such as **Coalesce**, **Split**, **Imit**, **MuConflict**, and **ImitCycle**. We have implemented the procedure in [Maude](http://maude.cs.illinois.edu/), a high performance reflective language.

For description of the BSM procedure, also know as BSM' in the paper, the reader is directed to the paper below.
* Ajay K. Eeralla, Serdar Erbatur, Andrew M. Marshall, Christophe Ringeissen. [Unification in Non-Disjoint Combinations with Forward-Closed Theories (extended verison)](http://members.loria.fr/CRingeissen/files/papers/combi-fc.pdf).


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
 > red in myBSMp : bsmUnify ( UnPr , RWS, BAL, N, SUB ) 
 ```
 
 where `UnPr` is an unification problem, `RWS` is a rewrite system, `BAL` is a data structure that keeps tracking the box-status of the terms (`Empty` at the begining), `N` is a new-variable-counter (`0` initially), and `SUB` is the substitution or solution. Of course, `SUB` is `none` at the begining.

<!---## Tested Results --->

Unification Problem | Rewrite System | Solution | Real Time (ms)
------------ | ------------- | ------------- | ------------- 
`'f['x:Nat , 'y:Nat]  =? 'y:Nat`| `emptyrs` | `fail` | `0` 


## Authors

* Ajay Kumar Eeralla, University of Missouri-Columbia (USA)
* Serdar Erbatur, Ludwig-Maximilians-Universita ̈t Mu ̈nchen (Germany)
* Andrew M. Marshall, University of Mary Washington (USA)
* Christophe Ringeissen, Universit ́e de Lorraine, CNRS, Inria, LORIA (France)

