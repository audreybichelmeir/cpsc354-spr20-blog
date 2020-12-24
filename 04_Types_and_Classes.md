# 04. Types and Classes
**Basic concepts **

A **type** is a collection of related values

**v :: T** to mean that **v** is a value in the type **T**, and say that v has type T

the symbol **::** can also be used with expressions that have not yet been evaluated

**Basic types**

**Bool** – logical values

This type contains the two logical values False and True.

**Int** – fixed-precision integers

This type contains integers such as -100, 0, and 999, with a fixed amount of memory being used for their storage

**Integer** – arbitrary-precision integers

This type contains all integers, with as much memory as necessary being used for their storage,thus avoiding the imposition of lower and upper limits on the range of numbers

**List type**

A list is a sequence of elements of the same type, with the elements being enclosed in square parentheses and separated by commas.

We write [T] for the type of all lists whose elements have type T. For example:

```
[False,True,False] :: [Bool]
```

The number of elements in a list is called its **length**.

The list [] of length zero is called the empty list, while lists of length one, such as [False] and [[]] are called **singleton** lists

*** NOTE: Note that [[]] and [] are different lists, the former being a singleton list

comprising the empty list as its only element, and the latter being simply the empty list that has no elements.

**F unction Types**

A function is a mapping from arguments of one type to results of another type

t1 → t2 is the type of functions that map values of type t1 to values to type t2.

*** NOTE: The arrow → is typed at the keyboard as ```->```

Example:
```
add :: (Int,Int) -> Int
add (x,y) = x+y
```
