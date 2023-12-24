# Token format

[Token](https://github.com/SymboScript/SymboScript/blob/main/types/src/lexer.rs#L4-L15)

```rust
pub struct Token {
    /// Token Type
    pub kind: TokenKind,

    /// Start offset in source
    pub start: usize,

    /// End offset in source
    pub end: usize,

    pub value: TokenValue,
}
```

[TokenValue](https://github.com/SymboScript/SymboScript/blob/main/types/src/lexer.rs#L110-L114)

```rust
pub enum TokenValue {
    None,
    Number(f64),
    String(String),
}
```
