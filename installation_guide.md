# Installation Guide

## 1. Installation

To install this extension, use the Gemini CLI `extension install` command. You can install it directly from the Git repository or from a local path.

### From Git (Recommended)
```bash
gemini extension install https://github.com/ryar001/AGENT-md-template
```

### From Local Path (For Development)
If you have cloned the repository locally:
```bash
gemini extension link .
```
*(Run this command inside the `AGENT-md-template` directory)*

## 2. Dependencies & Auto-Installation

This extension relies on the **`dev-tools`** MCP server to provide advanced tracking capabilities (via `run_ai_tracker`).

**Good news!** You do **not** need to install `dev-tools` manually. 

When you install this extension, the `dev-tools` MCP server is **automatically configured** for you. The extension definition includes the necessary configuration to run `dev-tools` using `uvx`.

### How it works
The `gemini-extension.json` file contains the following configuration:

```json
"mcpServers": {
    "dev-tools": {
        "command": "uvx",
        "args": [
            "dev-mcp"
        ]
    }
}
```

This tells the Gemini CLI to automatically register the `dev-tools` server when the extension is loaded.

## 3. Verification

To verify that the extension and its dependencies are installed correctly:

1.  **Check Extension Status**:
    ```bash
    gemini extension list
    ```
    Ensure `agent-md-template` is listed and enabled.

2.  **Check MCP Server**:
    The `dev-tools` server should be initialized automatically when you start a session or run a command that requires it.

3.  **Test Command**:
    You can run the `/track` command to verify that the `ai-tracker` tool (provided by `dev-tools`) is working:
    ```bash
    /track
    ```
