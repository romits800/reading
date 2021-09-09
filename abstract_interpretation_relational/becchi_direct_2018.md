| **Title**     | A Direct Encoding of NNC Polyhedra                               |
|:-------------:|------------------------------------------------------------------|
| **Authors**   | Anna Becchi and Enea Zaffanella                                  |
| **Venue**     | CAV'18                                                           |
| **Tool**      |  Parma Polyhedra Library                                         |
| **Reading level** | Medium                                                       |



# Summary
The paper presents a **direct** encoding of Not Necessary Closed (NNC) Polyhedra.
NNC Polyhedra allow strict inequalities (< or >) that is not allowed in 
Closed Polyhedra analysis like the invariant generation of 
[cousot_automatic_1978.md](../automatic_invariant_generation/cousot_automatic_1978.md).

The direct encoding represents the NNC Polyhedra with two representations,
i) a *skeleton representation* that merely consists of the "closed" polyhedra that 
forms the area and ii) a **non skeleton representation** that consists of 
the bounderies that are included in the polyhedron.

This *direct* representation is opposed to previously proposed *indirect* representation
that requires a so-called ε-representation that uses an additional space dimension.

The paper presents a conversion Chernikova-like algorithm to convert from constraints 
to generators.

# Contributions
Presents the direct representation of NNC Polyhedra and a conversion algorithm from
constraints to generators (discusses the duality of the generators to constraints algorithm).
The algorithm seems to lead to significant improvement for NNC but also Closed Polyhedra for
the examined benchmarks.

# Evaluation
Makes two experiments, the first on closed polyhedra and the second on NNC polyhedra.
The first experiment shows that there is no overhead on closed polyhedra, 
it actually seems slightly better.
The second experiment shows that the *direct* representation 
improves the efficiency compared 
to the ε-representation algorithm.

# Tool
Check also PPLlite used in a follow-up paper.

# TODO
Read and understand better the conversion algorithm.
