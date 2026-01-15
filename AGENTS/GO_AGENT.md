# Go Development Standards

## 1. Coding Standards (Hard Constraints)
*   **Style**: Strict `gofmt` and `goimports`.
*   **Documentation**: GoDoc comments for all exported members.
*   **Error Handling**: Idiomatic checks (`if err != nil`). No panic in production code.
*   **Modularity**: "Accept interfaces, return structs". Keep packages small and focused.

## 2. Environment & Tooling
*   **dependency Management**: Use Go Modules (`go.mod`).
*   **Testing**: Standard `testing` package with table-driven tests.
*   **Preferred Stack**:
    -   Gin or Echo (Web Framework).
    -   Cobra (CLI), Viper (Configuration).
    -   GORM or sqlc (Database).
