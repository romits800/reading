| **Title**     | Decomposition instead of self-composition for proving the absence of timing channels |
|:-------------:|--------------------------------------------------------------------------------------| 
| **Authors**   | Timos Antonopoulos, Paul Gazzillo, Michael Hicks, Eric Koskinen, Tachio Terauchi, and Shiyi Wei |
| **Venue**     | PLDI'17                                                                              |
| **Tool**      | Blazer (Not found)                                                                   |
| **Rel. Analysis** | k-safety/decomposition                                                           |
| **Reading level** | Medium/High                                                                      |



# Summary

This paper presents a decomposition-based appoach for solving  k-safety problems, including
a detailed example on timing attacks.
First the algorithm iterates on two steps:
- decomposition of the program in parts that are equivalent with regards to the
k-safety problem, e.g. for timing attacks low-equivalent blocks.
- check a property, e.g. the algorithms execution time for timing attacks.

If after these iterations, it is not possible to prove that the program is safe, 
the algorithm follows another iterative procedure to identify an attack.
- decomposition of the program for the attack, e.g. for timing attacks high-equivalent blocks.
- check whether there is an attack, e.g. high-dependent significant timing variations.


Theoretically the approach is sound and complete.

# Evaluation
Uses own-designed benchmarks and more benchmarks (TODO).


