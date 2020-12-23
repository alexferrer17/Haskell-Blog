# ARS week 2

This section will mostly be all the definitions that are important for an abstract reduction system. We get a better understanding on how ARS work.

## Definitions

Let (A, ->) be an ARS and let a,b range over A

* `a` and `b` are equivalent if `a` is the reflexive, symmetric and transitive closure of `b`.
* `a` is reducible if there is a `b` such that `a` -> `b`
* `a` is a normal form is `a` is not reducible. We also say that `a` is not reducible.
* `a` reduces to `b` if `a` is the reflexive and transitive closure of `b`.
* `a` has a normal form `b` if `a` reduces to `b` and `b` is a normal form.
*  If `a` has exactly one normal form of `a` we say that `a` has a unique normal form.
*  If every element has a unique normal form then we say `A` has unique normal forms.
* `a` `b` are joinable if `a` and `b` reduce to the same element .
* (A, ->)
⋅⋅* Church-Rosser if all equivalent elements are joinable
⋅⋅* Confluent if whenever x reduces to y and z, then y and z are joinable
⋅⋅* terminating if there is no infinite chain. ()
⋅⋅* Normalising, or has a normal form, if every element has a normal form
