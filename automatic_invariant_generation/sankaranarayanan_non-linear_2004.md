| **Title**     | Non-Linear Loop Invariant Generation using Gröbner Bases     | 
|:-------------:|--------------------------------------------------------------| 
| **Authors**   | Sriram Sankaranarayanan and Henry B. Sipma and Zohar Manna   | 
| **Venue**     | POPL'04                                                      |
| **Tool**      | Not found                                                    |
| **Invariant** | Polynomial                                                   |
| **Reading level** | Medium/High                                              |

# Summary
A method to generate *non-linear* (or algebraic) invariants for a program.

## Preliminaries
Defines:

* *Algebraic assertions* and *Ideals*.
* *Terms* and *Reduction*
* Gröbner Basis, G, of an Ideal is a basis that we can use to prove
  that $p \in I$: To find G we use *Bucheberger Algorithm*.
  - library GROEBNER
  - With this basis all reductions of ![equation](http://www.sciweavers.org/tex2img.php?eq=p%5cin%20I&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=)
 will yield a normal form 0, i.e.
	that `p` is a member of `I`.
* *Templates* are parametric polynomials
* If `η` is an *inductive assertion map*, then `η(l)` is an invariant at
  position `l`.

## Constraint Solving

From the paper: "Given an algebraic transition system with a template map, compute con-
straints on the template variables A, such that any solution to these
constraints specializes the template to a valid inductive assertion
map."


Given a transition system, we calculate the *initiation* and
*consecution* steps.  These correspond to the constraints for the
initial values and the inductive steps, respectively.
For the consecution case, the exact approach for the enabled case
(where we have a taken branch) results into non-linear constraints 
that make the final constaint problem intractable.

To overcome this problem the paper proposes simplifiying the
problem by assuming differnt pattern relationships for the
consecution case. 
This leads to parametric linear constraints, where the parameters need to
be eliminated, which can be done efficiently in the general case.
Otherwise, one must come up with additional, redundant constraints
to assist the process.
This approach does not deal with inequalities, but generates non-linear
invariants.
