# Parser

## Expressionss

### Operator priority

| Operator/Expression                     | Associativity | Parser fn name | Evaluation priority | Implementation |
| --------------------------------------- | ------------- | -------------- | ------------------- | -------------- |
| `!` `++` `--` `()` Literals Identifiers | Left to Right | factor         | 1                   | ✅             |
| `^`                                     | Left to Left  | power          | 2                   | ✅             |
| `*` `/` `%`                             | Left to Right | term           | 3                   | ✅             |
| `+` `-`                                 | Left to Right | add_sub        | 4                   | ✅             |
| `>>` `<<`                               | Left to Right | shift          | 5                   | ❌             |
| `<` `<=` `>` `>=` `==` `!=`             | Left to Right | cmp            | 6                   | ❌             |
| `&`                                     | Left to Right | bit_and        | 7                   | ❌             |
| <code>\|</code>                         | Left to Right | bit_or         | 8                   | ❌             |
| `==` `!=` `<` `<=` `>` `>=`             | Left to Right | cmp            | 9                   | ❌             |
| `&&`                                    | Left to Right | logical_and    | 10                  | ❌             |
| <code>\|\|</code>                       | Left to Right | logical_or     | 11                  | ❌             |
