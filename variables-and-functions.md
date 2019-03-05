# Variables and Functions

```scheme
(def foo 0)
```

This will define a variable in the current module named `foo` to the value 0. def will also overwrite the closest variable of the same name, so it can change the value of a function argument or a let binding value as well.

### Defining Functions

A function literal can be created with the `fn` form:

```scheme
(fn (x y)
  (+ x y))
```

This creates a function literal which when called with 2 arguments, returns their sum. You can define a variable to a function as,

```scheme
(def add (fn (x y)
            (+ x y)))
```

But this is a little bit too much to type every time for something thats important as a function binding, so there's a macro for that \(and an overloaded `def`\):

```scheme
;; All these things do the same exact thing:
(def add (fn (x y)
            (+ x y)))
(defn add (x y)
   (+ x y))
;; The overloaded def syntax...
(def (add x y)
   (+ x y))
```

I'm particularly a fan of the overloaded `def` syntax because the funciton signature represents the calling syntax. You would call add with `(add 1 2)` which looks alot like the signature when you define it.

You'll also notice that there is no type information in functions.

