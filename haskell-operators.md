| Operator(s)         |  Precedence | Associativity | Description |
-------------------------------------------------------------------
.                     | 9           | right         | function composition
!!                    | 9           | left          | list indexing
^, ^^, **             | 8           | right         | exponentiation (integer, fractional, and floating-point)
*, /                  | 7           | left          | multiplication, division
+, -                  | 6           | left          | addition, subtraction
:                     | 5           | right         | cons (list construction)
++                    | 5           | right         | list concatenation
`elem`, `notElem`     | 4           | left          | list membership
==, /=, <, <=, >=, >  | 4           | left          | equality, inequality, and other relation operators
&&                    | 3           | right         | logical and
||                    | 2           | right         | logical or
>>, >>=               | 1           | left          | monadic bind ignoring the return value, monadic bind piping value to the next function
=<<                   | 1           | right         | reverse monadic bind (same as above, but arguments reversed)
$                     | 0           | right         | infix function application (f $ x is the same as f x, but right-associative instead of left)
