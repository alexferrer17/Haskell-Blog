#Hoare Logic

Lastly for the final post we are going to go over the Hoare Logic or at least an introduction to it.


## Definition:

`Hoare Logic` is a formal system with a set of logical rules for reasoning rigorously about the correctness of computer correctness. This grew out of structured programming.
I thought the Hoare Triple was interesting.


## The Hoare Triple:

The Hoare triple talks about how the execution of a piece of code changes the state of the computation.

This is the form of a Hoare Triple:

```
{P}C{Q}
```
Where P and Q are assertions in this case and C is the command. Basically means that when the P is the precondition and Q is the postcondition while executing the command establishes the postcondition.

These are the axioms that other imperative programming languages have adapted so they can make rules like `concurrency`, `procedures`, `jumps` and `pointers`.
