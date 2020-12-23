# Calculator that works on Concrete syntax

We proved that we could do a simple calculator with just Haskell data types, recursion and pattern matching. Sometimes that can be harder, specially trying to do two dimensional operations all the time. That's why having a concrete syntax helps you simplify your operaitons operations.


For example instead of doing this:
```
Plus (Num 1) (Times (Num 2) (Num 3))
```
we can do something like this:
```
1 + 2 * 3
```

This seems way easier right? We just need to find a way to make this happen,
the good news is that is has already been done, it is called parsing.

## Parsing

Parsing literally means analyzing a string of symbols into it's constituents, which creates a parsed tree that shows a relation in its syntax.

For the example we did with adding it would have a tree like this:

```
Plus
  / \
Num   Times
|      / \
1   Num   Num
     |     |
     2     3
```

To put this into practice what we do is to create a set of rules that defines our arithmetic expressions like +, *, (, ). This is called a context-free grammar.

```
Exp -> Exp '+' Exp1                                
Exp -> Exp1                                        
Exp1 -> Exp1 '*' Exp2                              
Exp1 -> Exp2                                       
Exp2 -> Integer                                         
Exp2 -> '(' Exp ')'
```

We can see if a string is in our language if it comes from our start symbol, in our case is the `Exp` and the symbols that we are going to use are the ones that are enclosed in these statement. The order in this case does matter.


Parsing is like a translator that will translate our abstract syntax into a more readable syntax . We are going to use the parser generator called `BNFC`.
This Parser generator takes an input a context-free grammar and produces a parser as an output. In BNFC we can do something like this:

```
Plus.   Exp ::= Exp "+" Exp1 ;
Times.  Exp1 ::= Exp1 "*" Exp2 ;
Num.    Exp2 ::= Integer ;
```
