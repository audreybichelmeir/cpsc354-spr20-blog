# 05. Defining Functions

**Pattern matching**

Choose between a sequence of results of the same type.

If the first pattern is matched, then the first result is chosen;

otherwise, if the second is matched, then the second result is chosen, and so on.

```
not :: Bool -> Bool
not False = True
not True = False
```

**List patterns**

Internally, every non-empty list is constructed by repeated use of an operator (:) called “cons” that adds an element to the start of a list.

 [1,2,3]

 { list notation }

 1 : [2,3]

 { list notation }

 1 : (2 : [3])

 { list notation }

 1 : (2 : (3 : []))

 That is, [1,2,3] is just an abbreviation for 1:(2:(3:[])).

 To avoid excess parentheses when working with such lists,the cons operator is assumed to associate to the right.

 For example, 1:2:3:[] means 1: (2:(3:[])).

Functions on lists can be defined using x:xs patterns.
```
head :: [a] ->
a head (x:_) = x
```

```
tail :: [a] -> [a] tail
(_:xs) = xs
```

head and tail map any non-empty list to its first and remaining elements.

*** NOTE:

x:xs patterns only match non-empty lists:
```
> head []
```
*** Exception: empty list
x:xs patterns must be parenthesised, because application has priority over (:).

For example, the following definition gives an error:

```
head x:_ = x
```

**Lambda Expression**

Functions can be constructed without naming the functions by using lambda expressions

λx → x + x

``` \ ``` represents the Greek letter lambda, written as λ.
takes a number x and returns the result x + x.
```
> (\x -> x + x) 2
4
```

```
add :: Int -> Int -> Int
add x y = x + y
```

can be understood as meaning

```
add :: Int -> (Int -> Int)
add = \x -> (\y -> x + y)
```
