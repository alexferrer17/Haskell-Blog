# Abstract Reduction Systems

In this week we will take care on what abstract reduction systems.
To make sure we are on the same page I will try to explain what they are and why do we use them.

`Abstract reduction systems`: It's a way of specifying a set of objects and rules that can be applied to transform them.

Basically it's the relationship that a set of objects has that we can use to reduce them to make them easier to understand.

Take for example a set:

```
S = {a,b,c}
```
and the relations be:

```
a-> bc
b -> c
c ->

```
If we had a system like this:

```
abb
```
We could reduce it to:
```
bcbb
ccbb
cccb
cccc

```
It would become an empty list in this ARS which makes it
We can now use these rules to reduce forms. For the next section we will go over all the rules that applied to ARS and all the information we can get from one ARS. Before that it is important to know what normal forms are.

##Normal forms

Normal form: `a` is a normal form is `a` is not reducible. In our last example the empty list is an example of a normal form since it cannot be reduced.
