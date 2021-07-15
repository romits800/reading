# Paper Title: Algorithm Selection for Dynamic Symbolic Execution: A Preliminary Study
**Authors**: Roberto Amadini, Graeme Gange, Peter Schachte, Harald S\o ndergaard, and Peter J. Stuckey


# Summary
This paper proposes a method to combine *Dynamic Symbolic Execution*
(DSE) with *Algorithm Selection* (AS), where an algorithm is a
constraint solver.
<!-- % -->
The application of the approach is test-case generation for
*JavaScript* programs using DSE with a portfolio of solvers.
<!-- % -->
Their approach uses a solver portfolio and includes information
exchange between the solvers to achieve high test-case coverage.


In particular, the approach uses multiple solvers running sequentially and
each of them returns a solution that corresponds to a test case.
<!-- % -->
In the proposed approach, \textsc{Aratha$^{++}$}, the solver takes as
input the solution of the previous solver and uses it as a ``no
good''. 
<!-- % -->

The main novelty of the approach is enabling information exchange
between the solvers, which improves the test-case coverage of the
programs compared to the state of the art.



# Evaluation 
The preliminary evaluation compares the proposed configurations with
single solver DSE and shows that \textsc{Aratha$^{++}$} performs best
with regards to coverage of statements and lines of code.
<!-- % -->
In particular, the evaluation compares two portfolio approaches
**without** information exchange (\textsc{Aratha$^+$}) and **with**
(\textsc{Aratha$^{++}$}) and shows that information exchange improves
the test-case coverage.


The paper proposes more advanced approaches for selecting the
appropriate solver that are, however, not included in the
(preliminary) evaluation of this paper.

