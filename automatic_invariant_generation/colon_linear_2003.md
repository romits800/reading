| **Title**   | Linear Invariant Generation Using Non-linear Constraint Solving  |
|:-----------:|------------------------------------------------------------------| 
| **Authors** | Michael A. Colón, Sriram Sankaranarayanan, and Henny B. Sipma    |
| **Venue**   | CAV'03                                                           |
| **Tool**    | Not found                                                        |



# Summary
A method to generate linear invariants using Farkas’ Lemma that allows
to generate an inequality that is an invariant from a system of inequalities.
<!--  -->
This system of inequalities consists of the transfer functions in the program
and for loops, a number of equations that correspond to different point(s) of
the loop(s).
<!--  -->
In particular, the approach defines a set of program points, the
**cutset**, where every cyclic path passes through some location
in the **cutset**.
<!--  -->
This generated inequality corresponds to an inductive invariant and
can be calculated using the system of equations and Farkas' Lemma
and a constraint solver.


This invariant has the form:

\begin{equation*}
c_1 * x_1 + ... + c_n * x_n + d \le 0
\end{equation*}


The constraint model finds solutions for parameters $c_i$ after eliminating
the variables $x_i$ from the system of equations.


# Evaluation

Compares with cousot_automatic_1978.md and evaluates on simple
programs with loops (also nested) like *heapsort*.

- No performance comparison with Abstract Interpretation.
- According to the SAS'04 paper (sankaranarayanan_constraint_2004.md), 
  this method is complete but very slow.

# Other work
A master's thesis (see larraz_hurtado_automatic_2011.md) uses SMT
solver to solver this problem and resolves after adding the new
constraints to the previous system of inequalities to get different
invariants.

- Can we just find all solutions in a normal constraint solver rather
  than SMT?


