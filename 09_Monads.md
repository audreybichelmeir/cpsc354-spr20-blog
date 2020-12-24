# 09. Monads

**Monads**

Consider the following type of expressions that are built up from integer values using a division operator:
```
data Expr = Val Int | Div Expr Expr
```

Such expressions can be evaluated as follows:
```
eval :: Expr -> Int
eval (Val n) = n
eval (Div x y) = eval x ‘div‘ eval y
```

However, this function does not take account of the possibility of division by zero, and will produce an error in this case:
```
> eval (Div (Val 1) (Val 0))
```
*** Exception: divide by zero

In order to address this, we can use the Maybe type to define a safe version of division that returns Nothing when the second argument is zero,
```
safediv :: Int -> Int -> Maybe Int
safediv _ 0 = Nothing
safediv n m = Just (n ‘div‘ m)
```
and modify our evaluator to explicitly handle the possibility of failure when the function is called recursively on the two argument expressions:
```
eval :: Expr -> Maybe Int
eval (Val n) = Just n
eval (Div x y) = case eval x
of Nothing -> Nothing
Just n -> case eval y of
Nothing -> Nothing
Just m -> safediv n m
```
Now, for example, we have:
```
> eval (Div (Val 1) (Val 0))
Nothing
```
monad provides the infrastructure for sequencing and naming used in the ```do``` notation.

```do``` notation allows us to write programs which perform I/O while calculating results

```
eval :: Expr -> Maybe Int
eval (Val n) = Just n
eval (Div x y) = do n <- eval x
m <- eval y
mn in turn, and then combine their result values x1
safediv n m
```
