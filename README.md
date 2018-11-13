### Basic Syntactic Mutation ###


The Basic Syntactic Mutation (BSM) procedure consists of inference rules such as **Coalesce**, **Split**, **Imit**, **MuConflict**, and **ImitCycle**. We have implemented the procedure in [Maude](http://maude.cs.illinois.edu/), a high performance reflective language.


### Prerequisites ###
To run the algorithm you will need to have installed Maude. 

### Install ###
Download and install Maude from here [Download Maude](http://maude.cs.illinois.edu/w/index.php?title=The_Maude_System).

### Instructions to run the program ###
Download .maude files to a directory. Run the maude on your machine and navigate to directory where the files reside in. 

1. #### Load the file using the following command ####

 ``` load _filename.maude_ . ```

2. #### Testing ####

 ```red in myBSMp : bsmUnify ( UnPr , RWS, BAL, N, SUB ) .```
 
 where ```UnPr``` is an unification problem to solve, ```RWS``` is a rewrite system, ```BAL``` represents an empty data structure which eventually tracks the box-status of the terms (Empty at the begining), ``N`` is a new variable counter (0 initially), and ``SUB`` is the substitution or solution. Of course, ``SUB`` is ``none`` initially.

