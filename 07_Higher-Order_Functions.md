7. Higher-order functions - OK
Basic concepts
higher-order functions: a function that takes a function as an argument or returns a function as a result
twice :: (a -> a) -> a -> a
twice f x = f (f x)
For example:
> twice (*2) 3
12
Purpose:
- Common programming idioms can be encoded as functions within the language itself.
- Domain specific languages can be defined as collections of higher-order functions.
- Algebraic properties of higher-order functions can be used to reason about programs.
