| **Title**     | 	Methodologies for Quantifying (Re-)randomization Security and Timing under JIT-ROP                                          |
|:-------------:|-------------------------------------------------------------------------------------------------------------------------------|
| **Authors**   | Salman Ahmed, Ya Xiao, Kevin Z. Snow, Gang Tan, Fabian Monrose, and Danfeng(Daphne) Yao                                       |
| **Venue**     | CCS'20                                                                                                                        |
| **Tool**      |                                                    |
| **Reading level** | Medium/High                                                                                                               |



# Summary
The paper make an evaluation of randomization against JIT-ROP using different 
randomization granularity.

The four tools they use for their evaluation are the following:
- Zipr: (instruction-level randomization)
- SR: (function-level randomization)
- CCR (block-level randomization)
- MCR (function + register-level randomization)

For re-randomization they evaluate Shuffler.

The paper considers the quality of the gadgets based on whether other instructions corrupt the functionality of
the gadget by e.g. corrupting the data of a **mov** gadget after the move (i.e. there are other instructions after 
the main instruction of the gadget). 

# Evaluation
They evaluate the methods based on Turing completeness for different gadget sets 
(for gadget extraction and type identification, they
use [ropper](https://github.com/sashs/Ropper)) and show the following results:


- Re-randomization upper bound: The re-randomization upper bound is between 0.7 to 3.5 seconds in their experiments (clearly machine dependent)  
- Pointer leakage location: The leakage position of the pointer for JIT-ROP does not effect the Turing completeness of
  the gadgets but affects the time for finding a Turing complete set of gadgets.
- Gadget availability: *Instruction-level randomization* is able to break the Turing completeness, whereas the other methods, i.e. 
  function shuffling, basic-block shuffling, and function shuffling + register renaming are less effective.
- Performance overhead: They observe 23% overhead for Zipr, 10% for SR, 3% for CCR, and 10% for MCR
- Quality of Gadget Chain: They 


# Notes
- Confirms that gnu libc is not compilable with llvm.
- They used another version of libc, [musl-libc](https://musl.libc.org/)
- Their results show that instruction shuffling is efficient against gadgets.

