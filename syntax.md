# Syntax

Cedar is a dialect of lisp, so this means there's basically no syntax. Almost everything in cedar is a function or a macro around a very small set of core special forms. As you may have already seen with the print example shown before, cedar being a lisp means that all functions are prefix notation. So when you want to call a function, you put it first in the list then put the arguments.

```scheme
(function arg1 arg2 arg3 ...)
```

This is the case for every function or macro in cedar. Even math:

```scheme
(+ 1 2)     ; => 3
(- 1 2)     ; => -1
(* 3 2)     ; => 6
(/ 3 2)     ; => 1 (an int)
(/ 3.0 2.0) ; => 1.5 (a float)
(/ 2.0)     ; => 0.5
```

All numbers in cedar are either an integer \(64bit\) or a double precision floats \(also 64bit\). This means that when you do math with only ints, you will always get ints out, but as soon as you use a floating point number, floating point infection will happen and all results will be floats. So adding 1 + 1.0 will yield 2.0

