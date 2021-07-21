| **Title**     | Algebra-Based Synthesis of Loops and Their Invariants (Invited Paper)                     |
|:-------------:|-------------------------------------------------------------------------------------------| 
| **Authors**   | Andreas Humenberger and Laura Kovács                                                      |
| **Venue**     | VMCAI'21                                                                                  |
| **Tool**      | Aligator.jl in Julia ([repo](https://github.com/ahumenberger/Aligator.jl.git))            |
| **Invariant** | Polynomial                                                                                |


# Paper Title: Algebra-Based Synthesis of Loops and Their Invariants (Invited Paper)
**Authors**: Andreas Humenberger and Laura Kovács

# Summary
Discusses their approach(es) (i.e. Aligator.jl) to generate loop invariants automatically and do the opposite, 
synthesize loops from invariants using loop templates in a analogous manner.


## Invariant generation
They extract a system of C-finite recurrence equations describing loop updates and use Gröbner basis to compute 
the polynomial ideal that contains *equality* invariants of the loop.
"Any polynomial invariant of the given loop is then a logical consequence of the polynomials from the computed polynomial ideal basis".

## Steps
1) A non-deterministic single-path loop L is transformed into the regular expression π∗
2) Extract a system of C-finite recurrence equations for π∗.
3) Solve the resulting C-finite recurrences for π∗.
4) Derive closed forms.
5) Compute a polynomial ideal I of all polynomials p(x) such that p(x) = 0 is a loop
   invariant of L by using Gröbner basis computation to eliminate n from the ideal.

Look at the example.

## Related Work
- Has a good overview of the Related work.

