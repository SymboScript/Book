# Parser

## Expressionss

### Operator priority

| Operator/Expression                              | Associativity | Parser fn name | Impl |
| ------------------------------------------------ | ------------- | -------------- | ---- |
| Calls, Identifiers, Literals                     | Left to Right | call           | ✅   |
| Members                                          | Left to Right | dot            | ✅   |
| new                                              | Right to Left | new_expr       | ✅   |
| delete                                           | Right to Left | delete_expr    | ✅   |
| await                                            | Right to Left | await_expr     | ✅   |
| `!` `++` `--` `()` `~` (unary `-` `+`) `[]` `{}` | Left to Right | factor         | ✅   |
| `^`                                              | Left to Left  | power          | ✅   |
| `*` `/` `%`                                      | Left to Right | term           | ✅   |
| `+` `-`                                          | Left to Right | add_sub        | ✅   |
| `>>` `<<`                                        | Left to Right | shift          | ✅   |
| `&`                                              | Left to Right | bit_and        | ✅   |
| `bxor`                                           | Left to Right | bit_xor        | ✅   |
| <code>\|</code>                                  | Left to Right | bit_or         | ✅   |
| `==` `!=` `<` `<=` `>` `>=`                      | Left to Right | cmp            | ✅   |
| `&&`                                             | Left to Right | logical_and    | ✅   |
| <code>\|\|</code>                                | Left to Right | logical_or     | ✅   |
| `..`                                             | Left to Right | range          | ✅   |
| `?:`                                             | Right to Left | ternary        | ✅   |
| `=` `:=` `+=` `-=` `*=` `/=` `^=` `%=`           | Right to Left | assign         | ✅   |
| `,`                                              | None          | comma          | ✅   |

### Statements

| Statement                  | Parser fn name | Trigger token | Impl |
| -------------------------- | -------------- | ------------- | ---- |
| Variable declaration       | var_decl       | Let           | ✅   |
| Async function declaration | async_fn_decl  | Async         | ❌   |
| Function declaration       | fn_decl        | Function      | ✅   |
| Return statement           | return_stmt    | Return        | ✅   |
| Yield statement            | yield_stmt     | Yield         | ✅   |
| Break statement            | break_stmt     | Break         | ✅   |
| Continue statement         | continue_stmt  | Continue      | ✅   |
| If statement               | if_stmt        | If            | ❌   |
| While statement            | while_stmt     | While         | ❌   |
| For statement              | for_stmt       | For           | ❌   |
| Loop statement             | loop_stmt      | Loop          | ❌   |
| Try statement              | try_stmt       | Try           | ❌   |
| Throw statement            | throw_stmt     | Throw         | ❌   |
| Expression statement       | expr_stmt      | Other         | ✅   |
