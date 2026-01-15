# Python Development Standards

## 1. Coding Standards (Hard Constraints)
* **Style**: Strict PEP8 compliance. Use `black` for formatting.
* **Documentation**: Google-style docstrings for all public members. Internal logic should use `# Reason: [Explanation]` for non-obvious choices.
* **Type Safety**: 100% type hint coverage. Use `TypedDict` for complex literals and `Pydantic` for schema validation.
* **Modularity**: Strict **500-line limit** per file. If a file exceeds this, you must refactor and propose a module-based split immediately.

## 2. Environment & Tooling
* **Package Management**: Use `uv` exclusively. Never use `pip` or `conda` directly.
* **Virtual Env**: All commands must be prefixed or run within `.venv`. Confirm the presence of `pyproject.toml` before adding dependencies.
* **Preferred Stack**: 
    - StrEnum (Type Safety), Literal (Type Safety), TypedDict (Type Safety), Pydantic (Type Safety).
    - FastAPI (API), FastMCP (Context/MCP), NiceGUI (UI), SQLModel (ORM).
    - LangGraph (Agents), Guardrail-ai (Input/Output validation), RAGAs (RAG Agents Evaluation).
