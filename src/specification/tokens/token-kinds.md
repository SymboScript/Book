# Token Kinds

This chapter describes the token kinds used in the spec.

[Kinds](https://github.com/SymboScript/SymboScript/blob/main/types/src/lexer.rs#L18-L107)

```rust
pub enum TokenKind {
    Eof, // end of file
    Comment,
    Unexpected,

    Semicolon,
    Comma,
    Colon,
    Dot,

    // Operators
    Plus,
    Minus,
    Star,
    Slash,
    Power,
    Range,
    Modulo,

    // Bitwise operators (Keyword2Operator)
    BitAnd,
    BitOr,
    BitNot,
    BitXor,
    BitLeftShift,
    BitRightShift,

    // Unary operators
    PlusPlus,
    MinusMinus,
    Question,

    // Logic operators (Keyword2Operator)
    And,
    Or,
    Xor,
    Not,

    /// Assignments operators (+=, -=, *=, /=...)
    Assign,
    FormulaAssign,
    PlusAssign,
    MinusAssign,
    MultiplyAssign,
    DivideAssign,
    PowerAssign,
    ModuloAssign,

    // Comparison operators
    Equal,
    NotEqual,
    Less,
    LessEqual,
    Greater,
    GreaterEqual,

    // Brackets
    LParen,
    RParen,
    LBrace,
    RBrace,
    LBracket,
    RBracket,

    // Identifiers
    Identifier,

    // Literals
    Number,
    Str,

    // --- Keywords ---

    // Keyword literals
    True,
    False,

    // Keywords
    If,
    Else,
    While,
    For,
    Loop,
    Let,
    Return,
    Break,
    Continue,
    Function,
    In,
}
```
