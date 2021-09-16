| **Title**     | SubPolyhedra: A (More) Scalable Approach to Infer Linear Inequalities                                                         |
|:-------------:|-------------------------------------------------------------------------------------------------------------------------------|
| **Authors**   | Vincent Laviron and Francesco Logozzo                                                                                         |
| **Venue**     | VMCAI'09                                                                                                                      |
| **Tool**      | Code available @ [Microsoft research](https://www.microsoft.com/en-us/download/details.aspx?id=52306)                                |
| **Reading level** | Medium                                                                                                                    |



# Summary
This work defines a new abstract domain consisting of i) linear equations and ii) intervals.
They use slack variables to represent inequalities, e.g. x-y <= 0 becomes [x-y =β, β in [0,-inf]].

The paper defines the different operators like join and widening that have high accuracy.

For linear equations the reduction , ρ, uses Gaussian elimination. For intervals ρ is the identity function.
For the *SubPoly* domain it used either simplex or an approximation. The latter performs best.


# Evaluation
The evaluation verifies contracts from big Windows libraries like system.dll. They are able to prove most of the 
contracts.

# TODO
Understand the algorithms more precisely if need to implement.
