| **Title**     | InvGen: An Efficient Invariant Generator                                                  |
|:-------------:|-------------------------------------------------------------------------------------------| 
| **Authors**   | Ashutosh Gupta and Andrey Rybalchenko                                                     |
| **Venue**     | CAV'09                                                                                    |
| **Tool**      | Only binary: [InvGen](https://www.cse.iitb.ac.in/~akg/invgen/index.html)                       |
| **Invariant** | Linear                                                                                    |
| **Reading Level** | Basic                                                                                 |

# Summary
Tool papper that presents **InvGen**.
**InvGen** combines the method using Farkas' lemma [colon_linear_2003.md](colon_linear_2003.md) 
with an abstract interpretation 
(AI) analysis as frontend (not part of the same tool) that is based on [gupta_tests_2009.md](gupta_tests_2009.md). 
The abstract interpretation analysis step performs sequentially interval, 
octagon, and polyhedral domain analysis.
This improves the generated invariants.
 
## Tool 
The tool is only available as binary and takes as input the transition system. 
For generating the transition system from a function in C, they provide a tool performing
AI that finally generates the transition system that is the input to **InvGen**.


