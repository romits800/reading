| **Title**     | Constraint-Based Linear-Relations Analysis                                                |
|:-------------:|-------------------------------------------------------------------------------------------| 
| **Authors**   | Sriram Sankaranarayanan, Henny Sipma, and Zohar Manna                                     |
| **Venue**     | SAS'04                                                                                    |
| **Tool**      | Source code: [StinG](https://home.cs.colorado.edu/~srirams/research.html#GROUP)           |
| **Invariant** | Linear                                                                                    |

# Summary
Presents a constraint-based method for deriving loop invariants.
Presents a simplification method for solving constraints in the same method described 
in [colon_linear_2003.md](colon_linear_2003.md).
Describes the method and the constraint solving approach for deriving the invariants.
In same cases, using a previous invariant in the transition system results in stronger invariants.


# Evaluation

The paper compares their approach with the original Polyhedra 
widening operator (Cousot and Halbwachs) and a more recent and more accurate widening operator.
The source code contains the benchmarks they used to compare the approaches.

This paper gives an indication of the scalability of these methods for increasing number of 
variables. 
The benchmark with the largest number of variables contains 18 variables.

- How would the "Fast polyhedra abstract domain" paper improve the scalability?
