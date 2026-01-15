# JavaScript/TypeScript Development Standards

## 1. Coding Standards (Hard Constraints)
*   **Style**: Strict TypeScript. Use `ESLint` and `Prettier` for formatting.
*   **Documentation**: JSDoc for all public members.
*   **Type Safety**: Strict `noImplicitAny`. Use `Zod` for runtime validation.
*   **Modularity**: Strict **500-line limit** per file. Prefer functional composition over deep inheritance.

## 2. Environment & Tooling
*   **Package Management**: Use `npm`, `pnpm`, or `bun`. Prefer `pnpm` for monorepos.
*   **Testing**: Use `Vitest` for unit testing.
*   **Preferred Stack**:
    -   React (UI), Next.js (Framework), TailwindCSS (Styling).
    -   Zod (Validation), TanStack Query (Data Fetching).
    -   Fastify/Express (Backend if Node.js).
