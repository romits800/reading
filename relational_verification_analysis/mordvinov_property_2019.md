| **Title**     | Property Directed Inference of Relational Invariants   |
|:-------------:|----------------------------------------------------------------------------------------------|
| **Authors**   | Dmitry Mordvinov  and Grigory Fedyukovich |
| **Venue**     | FMCAD'19                                                                                       |
| **Tool**      |                                                                                              |
| **Rel. Analysis** | Relational Verification                                                                   |
| **Reading Level** | Basic                                                                           |
| **Approach** |  Constraint Horn Clauses - Model Checking (?)              | 
<!-- | **Invariant** | Relational Invariants                                         | -->




# Summary


This paper uses a technique called *Property directed reachability* (PDR) 
for solving systems of *Constraint Horn Clauses* (CHC) to verify relational  properties.

They propose a novel PDR-based
approach that maintains over- and under-approximations of
semantics for groups of predicates. 

<!-- It has the same effect -->
<!-- as after doing a product-program transformation, but without -->
<!-- actually transforming the system. --> 
They propose an algorithm that identifies groups of predicates on demand,
which allows for pruning of the search space and improved performance.

Their approach is similar and improves **Spacer** (Kumuravelli et al. CAV'14).



# Evaluation

- 840 safety problems (from paper Champion et al. Asian Symbosium of programming languages and systems '18), not derived from relational verification
- 37 relational verification problems derived from (Mordvinov et al. CoRR'17) 
