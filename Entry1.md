# IMPERATIVE VS FUNCTIONING PROGRAMMING: (Week 1)

In `Imperative programming` we instruct the computer what to do step by step.
In the other hand `Functioning programming` approaches problem solving as pure functional.

Personally I'm used to imperative programming languages like Python, Java or C so functional languages were something I never touched before. So it is useful to compere them side by side.


Lets take Python as an example for Imperative programming.
In python we assign operations that modifies the memory and we don't fully have
to understand what's going on inside the memory of it to be able to assign these operations.
Haskell in the other hand, everything is an expression that the computer then evaluates.
Functional models are much simpler than imperative programming ones.

NOTE: Python is imperative but was build from influences from `Haskell`.

Some features that functional languages have are:

*   `Pure functions`: Pure functions will always return the same outputs
*   `Immutability`: Data cannot change after creation. For example in a list with items you cannot change the number of elements
*  ` Higher Order Functions`: functions can take other functions as parameters and can return new functions as output. This allows abstract over functions.


## Pure function

For a pure function for example lets create a function that adds two to a list of numbers

```
def add_2_pure(numbers):
  new_numbers = []
  for n in numbers:1
    new_numbers.append(n + 2)
  return new_numbers

list_numbers = [1,3,6,8,6]
added_numebrs = add_2_pure(list_numbers)
```

added numbers will become `[3,5,8,10,8]` but list_numbers will still remain `[1,3,6,8,6]` since its not referencing any other variables outside the function the function is pure.

## Inmutability

Python offers lists that are immutable, they are called tuples in contrast they offer lists which are mutable

```
tuple = (1, 4, 3, 2)
```
## Higher Order Function

Lets do a function that prints a line multiple times:

```
def write_repeat(message, n):
  for i in range(n):
    print(message)
