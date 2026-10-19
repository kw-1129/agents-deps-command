# agents-deps-commend
A slash command / prompt for AI coding agents that analyzes a project's dependencies from a URL and generates a YAML manifest plus an interactive HTML dependency graph, saved to your Desktop. Works with OpenCode and some other AI agents.

This command is only compatible with agents that support Markdown-based slash commands.

## Output

By default, this command generates two files on your Desktop:

- `deps.yaml` — a machine-readable dependency manifest
- `deps.html` — an interactive dependency graph you can open in any browser

Nothing is installed automatically. These files are for you to review before deciding how to install dependencies.

## Installation
Run the following command to install this command into your OpenCode:
bunx opencode-marketplace install https://github.com/kw-1129/agents-deps-command
