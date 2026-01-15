## 2026-01-15
### Documentation
* AGENT.md: Added a note clarifying that file paths are relative to the AGENT.md file.

Refactor:
  gemini-extension.json:
    - Added 'extension' configuration for commands/extension.toml.
    - Added 'readme' configuration for commands/readme.toml.

2026-01-15

Chore:
  gemini-extension.json
    - Update version to 0.6.3.

What's New:
  commands/track.toml
    - Enhance track command to execute `run_ai_tracker` tool, including version synchronization logic.
    - The new workflow reads version files, runs the AI tracker, and updates configuration files and `UPDATES.md`.

**What's New:**
*   **commands/extension.toml**: Introduced `/extension` command for managing Gemini extensions. This includes installing from Git URLs and updating existing extensions. It also handles synchronization of extension rules (AGENT.md) and conversion of command TOML files to workflow MD files.

**Documentation Updates:**
*   **commands/debug.toml**: Updated command description for `/debug`.
*   **commands/init.toml**: Updated command description for `/init`.
*   **commands/overview.toml**: Updated command description for `/overview`.
*   **commands/plan.toml**: Updated command description for `/plan`.
*   **commands/preflight.toml**: Updated command description for `/preflight`.
*   **commands/task.toml**: Updated command description for `/task`.
*   **commands/test.toml**: Updated command description for `/test`.
*   **commands/track.toml**: Updated command description for `/track`.

**Project Update Log (2026-01-15)**

**What's New**
*   **commands/debug.toml**: Added `--help` text for the `debug` command.
*   **commands/init.toml**: Added `--help` text for the `init` command.
*   **commands/overview.toml**: Added `--help` text for the `overview` command.
*   **commands/plan.toml**: Added `--help` text for the `plan` command.
*   **commands/preflight.toml**: Added `--help` text for the `preflight` command.
*   **commands/task.toml**: Added `--help` text for the `task` command.
*   **commands/test.toml**: Added `--help` text for the `test` command.
*   **commands/track.toml**: Added `--help` text for the `track` command.

What's New:
gemini-extension.json
- Added 'overview' command configuration pointing to commands/overview.toml.
- Added 'extension' command configuration pointing to commands/extension.toml.

**New Feature**
*   `/AGENTS/GO_AGENT.md`: Defines Go development standards, tooling, and preferred stack.
*   `/AGENTS/JS_AGENT.md`: Defines JavaScript/TypeScript development standards, tooling, and preferred stack.
*   `/AGENTS/PYTHON_AGENT.md`: Defines Python development standards, tooling, and preferred stack.
*   `/AGENTS/RUST_AGENT.md`: Defines Rust development standards, tooling, and preferred stack.

**Refactor**
*   `AGENT.md`: Restructured agent instructions and added language-specific mapping.

**Enhancement**
*   `commands/test.toml`: Enhanced test workflow to include language detection, static analysis pre-flight check, and detailed coverage reporting.

**Configuration**
*   `.gitignore`: Added `.gemini` directory and test file comments to ignore list.

Chore:
    gemini-extension.json:
        Added "contextFileName": "AGENT.md" to configure context file.
        Version updated to 0.5.1.
    __version__.py:
        Version updated to 0.5.1.

What's New:
* commands/overview.toml: Added a new `overview` command for project documentation generation, including logic for architecture and feature documentation.

Refactor:
* commands/preflight.toml: Updated prompt to include using Google Search for library discovery.

Chore:
* Project version updated to `0.5.0`. This is reflected in `UPDATES.md` and `gemini-extension.json`.

Warnings:
None

Refactor:
* AGENT.md: Updated instructions for project overview and feature workflow management.
* README.md: Restructured command list and removed outdated "Global Instructions" mention.

What's New:
* README.md: New slash commands /overview, /debug, /plan added.
* gemini-extension.json: Registered plan and overview commands.

Chore:
* __version__.py: Version updated to 0.4.0.
* gemini-extension.json: Version updated to 0.4.0.

What's New (2026-01-07)
  commands/overview.toml:
    - Added 'overview.toml' defining a Project Documentation Generator command. This command automates the creation and updating of project documentation, including architecture and feature-specific markdown files, based on code analysis.
  AGENT.md:
    - Updated agent's workflow to include project overview and documentation management. Instructions are added for utilizing the new `/overview` command and maintaining documentation files like ARCHITECTURE.md and PROJECT_README.md.

Chore (2026-01-07)
  gemini-extension.json:
    - Updated extension version to "0.2.1".

What's New:
- New Command: 'overview'
  - Description: Generates and maintains project documentation (Architecture, README, Features) in `PROJECT_OVERVIEW`.
  - Files: `commands/overview.toml`

Configuration:
- Update: `gemini-extension.json`
  - Version: 0.2.1
  - Description: Registered `/overview` command integration in `AGENT.md`.

2026-01-07
Feat:
- commands/overview.toml:
  - Added logic for `/overview` command to analyze project structure and generate documentation.
- AGENT.md:
  - Added new "Project Overview & Documentation" section.
  - Added mandatory rules to run `/overview` if documentation is missing.

Chore:
- gemini-extension.json:
  - Bumped version to 0.2.1.

2026-01-02
Chore:
- Synced version to 0.1.3 to match extension manifest.
- Executed AI tracker via `uvx dev-mcp run_ai_tracker`; no bugs reported.

2026-01-02
Refactor:
  commands/track.toml:
    - Add instruction to run `/debug` if `ai-tracker` reports bugs.
    - Add instruction to create/update `UPDATES.md` with the changes made.

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
