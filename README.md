truthy
======

Small utility for parsing logic expressions and generating truth tables.


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
