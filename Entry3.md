# Calculator that works on Abstract syntax
## Calculators in Haskell
Calculators in Haskell are quite simple. They are build through Haskell data types, recursion and pattern matching.

Be ready to have your machine able compile and run Haskell files.

First let's take a look at how Data types work on Haskell.
### Data Types on Haskell
In Haskell, data types are declared like the following:

```
data variable = int
```
Note that the variable can store whatever datatype you want. This shows how `flexible` the language can be.

Also note that we cannot change the datatypes of the variables after we declared them. This is just like structs in other languages.

## Recursive types on Haskell

If we would want to prove how adding works based on successors numbers call them S, we could prove it by doing it with recursion.
 In Haskell first we have to declare the datatype that represents numbers or their successors:

```
data NN = O | S NN
deriving (Eq, Show)
```

then we can define how adding works:

```
    addNN :: NN -> NN -> NN
    addNN O n = n
    addNN (S n) m = S (addNN n m)
```


We could do the same for operations that work with successors for example multiplication.

```
    mult :: NN -> NN -> NN
    mult O n = O
    mult (S O) n = n
    mult (S n) m = add m (mult n m)
```

All this works since we created our own data type that allows us to have successors. As you can see the code is very similar to how definitions work on discrete mathematics.
