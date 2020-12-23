# RECURSIVE PROGRAMMING IN HASKELL: (WEEK 2)

After playing around with Haskell basic operations it seems to
me that is quite straight forward and reminds me of simple algebra.
Simple math can be quite simple to understand but understanding recursion was a little
bit more challenging.

First I had to understand how recursion works on numbers, I would start something
like this:

func 0 = ...
fun n = ...

This is similar to proving a recursion in discrete mathematics. In Haskell recursion is very
helpful because unlike imperative programming languages Haskell you use recursion to declare
what a function is. Let's try to define a recursion function in a mathematical way as an example first.

##Example:

For example lets start defining the famous fibbonacci equation
```
fib(0) = 0
fib(1) = 1
fib(n) = fib(n-1) + fib(n-2)
```



 ## Recursion in `Haskell`:

In Haskell instead of using loops we use pattern matching and recursion making it very similar to how mathematics works. The funny thing is that the same way we defined the fib sequence mathematical we defined it in haskell:

```
fib 0 = 0
fib 1 = 1
fib n = fib (n-1) + fib (n-2)
```
This is basically like the` hello world` of Haskell
