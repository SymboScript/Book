# Parser

## Expressionss

### Operator priority

| Operator/Expression                    | Associativity | Parser fn name | Impl |
| -------------------------------------- | ------------- | -------------- | ---- |
| Method calls                           | Left to Right | call           | ❌   |
| Function calls                         | Left to Right | call           | ❌   |
| `!` `++` `--` `()` `~`                 | Left to Right | factor         | ✅   |
| `^`                                    | Left to Left  | power          | ✅   |
| `*` `/` `%`                            | Left to Right | term           | ✅   |
| `+` `-`                                | Left to Right | add_sub        | ✅   |
| `>>` `<<`                              | Left to Right | shift          | ✅   |
| `&`                                    | Left to Right | bit_and        | ✅   |
| `bxor`                                 | Left to Right | bit_xor        | ✅   |
| <code>\|</code>                        | Left to Right | bit_or         | ✅   |
| `==` `!=` `<` `<=` `>` `>=`            | Left to Right | cmp            | ✅   |
| `&&`                                   | Left to Right | logical_and    | ✅   |
| <code>\|\|</code>                      | Left to Right | logical_or     | ✅   |
| `..`                                   | Left to Right | range          | ✅   |
| `?` `:`                                | Left to Right | ternary        | ✅   |
| `=` `:=` `+=` `-=` `*=` `/=` `^=` `%=` | Right to Left | assign         | ✅?  |
| `,`                                    | Left to Right | comma          | ✅   |
