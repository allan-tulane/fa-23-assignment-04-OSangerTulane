# CMPS 2200 Assignment 4
## Answers

**Name:**_________________________


1.a)
    find largest coin less than or equal to the amount that the user starts with.
    exchange coin for us currency amount so that you may repeat the process with your new number.
    repeats the process till your amount is $0.

  b)

    Greedy-selection property: Optimal choices are made at each step by consistently selecting the highest denomination coin. Since our denominations follow powers of 2, using a single larger coin is always more efficient than employing multiple smaller coins to achieve the same value. For instance, replacing one 2^k coin with two 2^(k-1) coins would yield the same amount but with more coins.

    Optimal substructure property: A problem exhibits optimal substructure when its optimal solution incorporates optimal solutions to its subproblems. Taking a 2^k coin leaves a reduced problem (N-2^k), to which the greedy algorithm consistently yields the best solution. As this holds true at every step, the final solution remains optimal.

    Using the largest coin doesn't block us from finding the best solution for the rest of the money. Since this is true at every step, the greedy algorithm must give us the best overall solution.

    
  c)
    W(n)=O(log n)

    S(n)=O(log n)


2.a)

    The greedy algorithm does not always give the least coins for random denominations. A counterexample is the set of denominations {1,3,4,5} for the amount 7. The greedy algorithm would choose two coins of 1 and one coin of 5, but the optimal solution is to use one coin of 3 and one of 4.


  b)

  
  An optimal solution created by its subproblems optimal solutions is referred to as "Optimal Substructure". In the context of the coin-changing problem, this implies that having an optimal solution for N dollars entails that, for any amount less than N, the included solution for that smaller amount must also be optimal.This means that for the coin-changing problem, if you possess an optimal solution for N dollars, then the solution encompassed for any amount less than N must also be optimal.

  If the solution for the smaller amount was not optimal, substituting it with an optimal solution for the smaller amount would result in a superior solution for N. This contradicts our assumption that we initially had an optimal solution for N.

  c)

  W(n) = O(nk)
  S(n) = O(n)




