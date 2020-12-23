#syntax of Lambda Calculus

We are going to learn how to build our first programming language. It's going to be called lambda calculus. Why would anybody want to do that you might ask?
Seems like a bunch, but actually easy with everything that we have learned so far. Partly because lambda calculus a mathematical way to express computations based on abstraction and substitution.

Lambda Calculus can even simulate the Turning Machine!  

##Programming language

A programming language is basically a set of vocabulary and grammatically words that instruct a computer how to perform a certain task. Since we were able to do an abstract calculator and a easier way to use it with a parser we are ready to start making this programming language.


## How this works:

Lambda Calculus has ONLY three programming constructs:

1.Variables: The basic programs are just variables like `e`.

2.Abstraction: If e is a lambda calculus with a variable x then
`λx.e` is the function of x. This would be the abstraction of x since the program e is not dependent of x anymore.

3.Application:  If we have two programs called e1 and e2 then
`e1e2` is the program that applies the function on e1 to e2 and not vice versa.

## Examples of lambda calculus programs:

Since lambda is not a character that we can type in a ASCII we are going to use
\. instead.

```
x
y
x y z
\.x.x
\x.x x
(\x (\y . x y)) (\x.x) z
```

# Semantics of the Lambda Calculus

Since now we know how part of the syntax works we will try to understand how to execute it.


Lets start with an example that uses substitution:

```
e::=λx.e∣ee∣x∣e+e∣e∗e∣0∣1∣2∣3∣6∣7
```

NOTE: Haskell does not let you take more than one parameter as an input, for substitution we use what's called `currying`, which replaces a function in two arguments by a function that takes one argument and returns a function that takes the second argument.
