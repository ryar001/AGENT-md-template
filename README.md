# Gemini CLI Agent Manifest

## Configuration
- **Global Instructions**: `AGENT.md`
- **Scripts Directory**: `scripts/`

## Slash Command Router

### `/init`
**Usage:** `/init`
Initialize or migrate project state. Analyzes workspace automatically.

### `/task`
**Usage:** `/task [Status Update]`
- `[Status Update]`: Optional status text to log (e.g., "Fixing bug").

### `/preflight`
**Usage:** `/preflight [Context]`
- `[Context]`: Optional. Specific libraries/methods to verify. Defaults to analyzing conversation history.

### `/test`
**Usage:** `/test [Target]`
- `[Target]`: Optional. Specific file or folder to test (e.g., `tests/test_main.py`). Defaults to full suite + static analysis.

### `/track`
**Usage:** `/track`
Transactional Checkpoint. Runs AI Tracker, bumps version, commits changes.

### `/overview`
**Usage:** `/overview [Path]`
- `[Path]`: Optional. Specify root directory if not current. Generates/Updates `PROJECT_OVERVIEW`.

### `/debug`
**Usage:** `/debug [Context]`
- `[Context]`: Optional. Error trace, file path, or bug description. Defaults to analyzing recent errors.

### `/plan`
**Usage:** `/plan <Goal>`
- `<Goal>`: Required. Description of feature/change (e.g., "Add user auth").

### `/extension`
**Usage:** `/extension <subcommand> <args>`
- `install <URL> [--global]`: Install extension from Git URL.
- `update <Name> [--global]`: Update existing extension.

### `/readme`
**Usage:** `/readme [--path <PATH>]`
- `[--path <PATH>]`: Optional. Specific path to the README file to update. Defaults to auto-detection.

## Usage
Trigger these specific workflows using the slash commands above. For general coding, refer to `AGENT.md`.