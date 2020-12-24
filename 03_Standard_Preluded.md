# 03. Standard preluded

**Basic Classes**

Equality types:
class Eq a where
(==), (/=) :: a -> a -> Bool
x /= y = not (x == y)

Ordered types:
Bool
Class Eq a => Ord a where
(<), (<=), (>), (>=) :: a -> a -> Bool
Min, max	           ::  a -> a -> a

**Booleans**

Type declaration:
data Bool = False | True deriving (Eq, Ord, Show, Read)

**Characters**

Type declaration:
data Char = ... deriving (Eq, Ord, Show, Read)

**Numbers**

Type declaration:
Data Int = …
		derving (Eq, Ord, Show, Read, Num, Integral)

**Lists**
Type declaration:
data [a] = [] | a:[a] deriving (Eq, Ord, Show, Read)
Select the first element of a non-empty list:
head :: [a] -> a head (x:_) = x
Select the last element of a non-empty list:
last :: [a] -> a last [x] = x last (_:xs) = last xs
