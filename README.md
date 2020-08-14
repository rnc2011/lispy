# lispy

lispy is a reimagining of Lisp implemented in Python with a focus on
readability. It is based on Peter Norvig's elegant [(How to Write a (Lisp)
Interpreter (in Python))](https://norvig.com/lispy.html).

## Define a variable

No parentheses!

```scheme
(define pi 3.14)
```

```lispy
define pi: 3.14
```

## Define a procedure

Whitespace!

```scheme
(define square (lambda r) (* r r))
```

```lispy
define square λ r:
    product r r
```

Note: lispy replaces `*` with `product` because most special characters are
reserved as infix operators. Likewise `λ` is used instead of `lambda`.

## Define a compound procedure

```scheme
(define circle-area (lambda (r) (* pi (* r r)))
```

```lispy
define circle-area λ r:
    product pi
        square r
```
