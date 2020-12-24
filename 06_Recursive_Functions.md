# 06. Recursive functions

**Basic concepts**

**Recursive**: it is to define functions in terms of themselves

```
fac :: Int -> Int
fac 0 = 1
fac n = n * fac (n-1)
```

fac maps 0 to 1, and any other integer to the product of itself and the factorial of its predecessor.

fac 3

= { applying fac }

3 * fac 2

= { applying fac }

3 * (2 * fac 1)

= { applying fac }

3 * (2 * (1 * fac 0 ))

= { applying fac }

3 * (2 * (1 * 1))

= { applying }

6

**Recursion on lists**

product maps the empty list to 1, and any non-empty list to its head multiplied by the product of its tail

```
product:: Num a => [a] -> a
product [] = 1
product (n:ns) = n * product ns
```

product [2,3,4]

= { applying product }

2 * product [3,4]

= { applying product }

2 * (3 * product [4])

= { applying product }

2 * (3 * (4 * product []))

= { applying product }

2 * (3 * (4 * 1))

= { applying }

24

length maps the empty list to 0, and any non-empty list to the successor of the length of its tail.
```
length :: [a] ® Int
length [] = 0
length (_:xs) = 1 + length xs
```

length [1,2,3]

= { applying length }

1 + length [2,3]

= { applying length }

1 + (1 + length [3])

= { applying length }

1 + (1 + (1 + length []))

= { applying length }

1 + (1 + (1 + 0))

= { applying }

3
