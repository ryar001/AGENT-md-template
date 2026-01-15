# Rust Development Standards

## 1. Coding Standards (Hard Constraints)
*   **Style**: Strict `rustfmt`.
*   **Linting**: Strict `clippy`. Treat warnings as errors.
*   **Safety**: Prefer safe Rust. Unsafe code must be heavily documented and isolated.
*   **Modularity**: Use workspace mechanism for multi-crate projects. 500-line limit per module.

## 2. Environment & Tooling
*   **Package Management**: `cargo`.
*   **Testing**: built-in `#[test]` and `cargo test`.
*   **Preferred Stack**:
    -   Tokio (Async Runtime).
    -   Axum (Web Framework).
    -   Clap (CLI), Serde (Serialization).
    -   SQLx or Diesel (Database).
