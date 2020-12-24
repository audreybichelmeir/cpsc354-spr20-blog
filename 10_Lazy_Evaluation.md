10. Lazy evaluation - OK
Introduction
• Avoids doing unnecessary evaluation;
• Ensures termination whenever possible;
• Supports programming with infinite lists;
• Allows programs to be more modular.
Evaluating strategies
square n = n * n
square (1+2) (apply + first)
square 3
3 * 3
9
this had 3 steps
Another evaluation
square (1+2) (appy square first)
(1+2) * (1+2)
3 * (1+2)
3 * 3
9 this had 4 steps
Any way of evaluating the same expression will give the same result, provided it terminates.


The outmost version is inefficient, because the argument 1+2 is duplicated when square is applied and is hence evaluated twice.

Due to such duplication, outermost evaluation may require more steps than innermost.

This problem can easily be avoided by using pointers to indicate sharing of arguments.

sldie 9 show

lazy evaluation = outermost evaluation + sharing of arguments
*** NOTE:
Lazy evaluation ensures termination whenever possible, but never requires more steps than innermost evaluation and sometimes fewer.
