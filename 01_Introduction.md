# Introduction to Haskell
**Functional programming Vs Imperative Language**
**Functional programming**
is style of programming in which the basic method of computation is the application of functions to arguments; A functional language is one that supports and encourages the functional style.

**Imperative Language**
in general, programming languages such as Java in which the basic method of computation is changing stored values.

To illustrate this an example, summing the integers 1 to 10

**Java:**
```
int total = 0;
for(inti=1;i< 10;i++)
total = total + i;
```
The computation method is variable assignment

**Haskell:**
```
sum [1..10]
```
The computation method is function application

**Features of Haskell**
**Concise programs**
- Having few keywords and by allowing indentation to be used to indicate the structure of programs

**Powerful type system**
- Requires little type information from the programmer, but allows a large class of incompatibility errors in programs to be automatically detected prior to their execution, using a sophisticated process called type inference

**List comprehensions**
- Comprehension notation that constructs new lists by selecting and filtering elements from one or more existing lists

**Recursive functions**
- Many computations have a simple and natural definition in terms of recursive functions, especially when pattern matching and guards are used to separate different cases into different equations

**Higher-order functions**
- Functions can freely take functions as arguments and produce functions as results

**Effectful functions**
- Provides a uniform framework for programming with effects, without compromising the purity of functions, based upon the use of monads.

**Lazy evaluation**
- Lazy evaluation ensures that programs terminate whenever possible, encourages programming in a modular style using intermediate data structures, and even allows programming with infinite structures.
