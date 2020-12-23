#Abstract Reduction Systems 3

In this week we take a look at what termination is and an example

## Termination:

`Termination`: This language attempts to use mathematical proof in verification of an algorithm. Termination plays a crucial role in having total correctness in  the measures.  Termination applies a measure into each step of the algorithm and uses a well-founded relation to see if it decreases. If the algorithm is functioning correctly, it should terminate because there are no infinite descending chains in respect to the well founded relation. Windows programs in the past are a good example of what would happen if the device driver went into an infinite loop, which was difficult to repair. Now with the Termination Abstract Reduction System, the loop is broken.  

An example of the loop termination analysis in an attempt to determine the type of behavior of a program which is dependent on the unknown input.

```
i : = 1
```

loop until `i = UNKNOWN`

```
i  : =  i  + 1
```

In this example the loop condition is defined using some value.  Where the value is UNKNOWN the termination analysis must take into account all the possible values of the UNKNOWN and try to discover if in case the UNKNOWN = 0, the termination cannot be shown.
