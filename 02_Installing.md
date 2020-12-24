# 02. Installing + Introduction to Haskell pt. 2
The interpreter can be started from the terminal command prompt ```$``` by simply typing ```ghci```:
The GHCi prompt ```>``` means that the interpreter is now ready to evaluate an expression

Example:
```
> 2+3*4
14
> (2+3)*4
20
> sqrt (3^2 + 4^2)
5.0
```
**Functional application**

For example, in mathematics the expression

f(a, b) + c d

means apply the function f to two arguments a and b, and add the result to the product of c and d.


For example, the expression above would be written in Haskell as follows:

f a b + c*d

functional application has higher priority than all other operators in the language (but that'll be discussed later)
For example, f a + b means (f a) + b rather than f (a + b).

Mathematics     \tHaskell
```
f(x)            fx
f(x,y)          f x y
f(g(x))         f (g x)
f(x,g(y))       f x (g y)
f(x)g(y)        fx*gy
```

scripting
files need the extension .hs, for example, test.hs
instruct GHCi system to load the new script:
```
$ ghci test.hs
```

commands to remember
:load name - load script name
:quit - quit GHCi

comments
scripts can also contain comments that will be ignored by the compiler
comments begin with the symbol -- and extend to the end of the current line
