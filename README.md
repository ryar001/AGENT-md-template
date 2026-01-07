# Gemini CLI Agent Manifest

## Configuration
- **Global Instructions**: `AGENT.md`
- **Scripts Directory**: `scripts/`

## Slash Command Router
- `/init`: `commands/init.toml` - Project State Manager (Bootstrap & Migration).
- `/task`: `commands/task.toml` - Task Management.
- `/preflight`: `commands/preflight.toml` - Research & Hallucination Guard (Docs verification).
- `/test`: `commands/test.toml` - Testing Orchestration (Pytest & .env.test).
- `/track`: `commands/track.toml` - Transactional Checkpoint (ai-tracker & BUGS_LOG).
- `/overview`: `commands/overview.toml` - Project Documentation Generator.
- `/debug`: `commands/debug.toml` - Deep Debugging Protocol.
- `/plan`: `commands/plan.toml` - Planning Assistant.

## Usage
Trigger these specific workflows using the slash commands above. For general coding, refer to `AGENT.md`.