truthy
======

Small utility for parsing logic expressions and generating truth tables.


Symbols
------
Propositional variables are a sequence of one or more uppercase letters.
Whitespace is ignored and parentheses can be used to disambiguate expressions manually.

Logical operators are:
  * and - `&`
  * biconditional - `<->`
  * conditional - `->`
  * not - `~`
  * or - `v`

Usage
------

```bash
$ echo '(A v B) -> B' | python -m truthy
((A v B) -> C)
+---+---+---+--+-----+---+----+----+----+
| A | B | C |  | ((A | v | B) | -> | C) |
+---+---+---+--+-----+---+----+----+----+
| T | T | T |  |  T  | T | T  | T  | T  |
| T | T | F |  |  T  | T | T  | F  | F  |
| T | F | T |  |  T  | T | F  | T  | T  |
| T | F | F |  |  T  | T | F  | F  | F  |
| F | T | T |  |  F  | T | T  | T  | T  |
| F | T | F |  |  F  | T | T  | F  | F  |
| F | F | T |  |  F  | F | F  | T  | T  |
| F | F | F |  |  F  | F | F  | T  | F  |
+---+---+---+--+-----+---+----+----+----+
```
