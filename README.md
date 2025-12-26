# Gemini CLI Agent Manifest

## Configuration
- **Global Instructions**: `GEMINI.md`
- **Scripts Directory**: `scripts/`

## Slash Command Router
- `/init`: `commands/init.toml` - Project State Manager (Bootstrap & Migration).
- `/task`: `commands/task.toml` - Task Management.
- `/preflight`: `commands/preflight.toml` - Research & Hallucination Guard (Docs verification).
- `/test`: `commands/test.toml` - Testing Orchestration (Pytest & .env.test).
- `/track`: `commands/track.toml` - Transactional Checkpoint (ai-tracker & BUGS_LOG).

## Usage
Trigger these specific workflows using the slash commands above. For general coding, refer to `GEMINI.md`.