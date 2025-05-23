# Project: Automated Testing Workspace

This project is designed for automated testing and result analysis. It provides a structured environment for writing, running, and managing tests, as well as storing test results and reference images.

## Project Structure

- `img/` — Reference images for UI or visual comparison tests.
- `results/` — Output files and test results (JSON, logs, etc.).
- `tests/` — Test cases, feature files, and documentation for test scenarios.

## Start Emulator
1. Open Android Studio.
2. Go to **Tools > Device Manager**.
3. Start the `Pixel 9` (or your desired) emulator.

Alternatively, from the terminal:
```zsh
# List available emulators
emulator -list-avds
# Start the Pixel 9 emulator (replace with your AVD name if different)
emulator -avd "Pixel_9_Pro_XL"
```

## MCP Configuration

Add the following to your configuration to define available MCP servers:

```json
"mcp": {
  "servers": {
    "playwright": {
      "command": "npx",
      "args": ["-y", "@playwright/mcp@latest"]
    },
    "sequential-thinking": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-sequential-thinking"]
    },
    "mobile-mcp": {
      "command": "npx",
      "args": ["-y", "@mobilenext/mobile-mcp@latest"]
    }
  }
}
```

## Start MCP Server

To start the MCP server:

1. Open the Command Palette (`Cmd+Shift+P`).
2. Search for `MCP: List`.
3. Select `Start MCP Server` from the list.

The server will start and listen for incoming test or agent requests.

## Running the Project with GitHub Copilot Agent Mode

To run and interact with this project using GitHub Copilot agent mode:

1. **Open the workspace in Visual Studio Code.**
2. **Enable GitHub Copilot agent mode** (if not already enabled):
   - Open the Command Palette (`Cmd+Shift+P` on macOS, `Ctrl+Shift+P` on Windows/Linux).
   - Search for and select `GitHub Copilot: Enable Agent Mode`.
3. **Interact with the Copilot agent**:
   - Use natural language prompts to run tests, analyze results, or generate new test cases.
   - Example prompts:
     - "Run all tests in the `tests/` folder."
     - "Compare the latest result in `results/` with the reference image in `img/`."
     - "Summarize the test results."

## Notes
- Ensure all dependencies for your test scripts are installed (see individual test files for requirements).
- Store new reference images in the `img/` directory for visual tests.
- Test results and logs will be saved in the `results/` directory.

---

For more details or custom automation, use the Copilot agent to explore or modify the workspace as needed.
