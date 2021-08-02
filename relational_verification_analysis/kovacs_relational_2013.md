| **Title**         | Relational abstract interpretation for the verification of 2-hypersafety properties |
|:-----------------:|-------------------------------------------------------------------------------------| 
| **Authors**       | Máté Kovács, Helmut Seidl and Bernd Finkbeiner                                      |
| **Venue**         | CCS'13                                                                              |
| **Tool**          | Not checked properly                                                                |
| **Rel. Analysis** | 2-hypersafety                                                                   |
| **Method**        | Abstract Interpretation                                                             |
| **Reading Level** | Basic                                                                           |



# Summary

Describes a new abstract interpretation analysis for the verification of
2-hypersafety properties. 
Their application if on medical data where the medical values should not 
interfere with the userdata or affect observations.

- Works for non-equivalent program executions.
- Uses the control-flow graph.
- Defines an abstract domain of the powerset of the program (product program)
  - Overapproximates the abstract value of a pair of nodes by computing the least upper bound for all possible pairs paths that reach these nodes.
- First finds the a good alignment for the two program executions.
