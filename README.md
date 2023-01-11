# SAT-solving
Davis-Putnam-Logemann-Loveland (DPLL) algorithm 
The algorithm 
This document outlines the algorithm implemented for SAT solving in the extra bonus 
component of ECE650 Assignment 2 (PA2). 
The algorithm is based on the Davis-Putnam-Logemann-Loveland (DPLL) algorithm, 
which is a complete, backtracking-based search algorithm for deciding the satisfiability of 
propositional logic formulae in conjunctive normal form (CNF). 
It works by recursively searching through the possible assignments of the variables in the 
CNF formula. The algorithm assigns a boolean value to each of the variables and then evaluates 
the formula. If the formula evaluates to true, then the formula is satisfiable. If the formula 
evaluates to false, then the algorithm backtracks and tries another assignment of the variables. 
The algorithm starts by assigning a value to each literal from the set of clauses. If a clause 
contains only one literal, then that literal is assigned a value. Otherwise, the literal with the 
highest frequency in the clauses is assigned a value. 
The algorithm then evaluates the formula. If the formula evaluates to true, then the 
algorithm returns true and the assignment of values is a satisfying assignment. If the formula 
evaluates to false, the algorithm then backtracks if the formula evaluates to false. It will then 
assign the opposite value to the literal with the highest frequency in the clauses and evaluate the 
formula again. This process is repeated until the formula evaluates to true or until there are no 
more possible assignments of values. If there are no more possible assignments of values, then 
the formula is not satisfiable. 
The algorithm also implements a conflict-driven clause learning (CDCL) technique. This 
technique is used to prune the search tree and reduce the number of possible assignments of 
values. This is done by maintaining a set of learned clauses. If a clause evaluates to false, then 
3 
the clause is added to the set of learned clauses. These clauses are then used to prune the search 
tree by preventing the algorithm from assigning values to literals which would make the formula 
evaluate to false. 
The algorithm also implements a variable ordering heuristic. This heuristic is used to 
reduce the number of possible assignments of values and improve the performance of the solver. 
This is done by assigning values to variables in the order of highest frequency in the clauses. 
Overall, this algorithm is an implementation of the DPLL algorithm with the added 
benefits of conflict-driven clause learning and variable ordering heuristics. This provides an 
efficient and complete SAT solver with improved performance.
