Chore:
- commands/test.toml:
  - Added detailed testing orchestration steps, covering sync, setup, standards, action, and analysis.
  - Introduced a markdown template for generating a test overview report.

2026-01-02
Chore:
- Synced version to 0.1.3 to match extension manifest.
- Executed AI tracker via `uvx dev-mcp run_ai_tracker`; no bugs reported.

2026-01-02
Refactor:
  commands/track.toml:
    - Add instruction to run `/debug` if `ai-tracker` reports bugs.
    - Add instruction to create/update `UPDATES.md` with changes made.

What's New
----------
2025-12-31
* commands/debug.toml: Added a new deep debugging command. This command defines a protocol for analyzing issues, creating a `DEBUG_PLAN.md`, seeking user review, and then executing the plan.

What's New
----------
GEMINI.md
- Added new mandatory workflow trigger for debugging: `/debug` command.

gemini-extension.json
- Registered the `debug` command.

GEMINI.md
  Refactor
    Updated preferred stack to include StrEnum, Literal, TypedDict, Pydantic for type safety, and LangGraph, Guardrail-ai, RAGAs for agents and validation.
  Chore
    Added mandatory workflow trigger for task completion tracking.

Warnings:
None found.

Refactor:
- `commands/track.toml`: Updated description for the 'track' command to clarify its goal of immediately executing the `run_ai_tracker` tool without delay or explanation.

Refactor: commands/track.toml
- Updated description for the 'track' command to detail a new workflow for transactional checkpoints. The new process involves executing `uvx dev-mcp run_ai_tracker --path .`, handling potential command failures, and iterating until no bugs are reported.

Warnings
- No breakpoints found.

Refactor
commands/test.toml:
  - Enhanced test orchestration with mandatory context synchronization and environment preparation steps.
  - Introduced immediate `pytest` execution with `-v` flag and pre-execution test fixing.
  - Added robust result analysis, logging failures to `BUGS_LOG.md` and providing a clear success message.

What's New
commands/track.toml:
  - Added configuration for `uvx dev-mcp` within `dev-tools`, including a prompt for user to install if not found.

2025-12-26

What's New
* gemini-extension.json:
    * Added extension configuration including name, version, description, context file, and command mappings.

2025-12-26
What's New
- GEMINI.md: Global Behavioral Guardrails and agent persona.
- README.md: Gemini CLI Agent Manifest and usage guide.
- commands/init.toml: Configuration for the /init command (Project State Manager).
- commands/preflight.toml: Configuration for the /preflight command (Research & Hallucination Guard).
- commands/task.toml: Configuration for the /task command (Task Management).
- commands/test.toml: Configuration for the /test command (Testing Orchestration).
- commands/track.toml: Configuration for the /track command (Transactional Checkpoint).
- gemini-extension.json: Extension configuration for the agent.

What's New
---------
*   2025-12-26: `__version__.py`
    *   Added `__version__ = "0.0.1"`.
