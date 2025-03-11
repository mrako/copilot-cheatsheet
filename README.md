# GitHub Copilot Cheat Sheet

GitHub Copilot is an AI-powered code completion tool that helps you write code faster and with fewer errors. This document covers essential keyboard shortcuts, slash commands, skills, and prompting tips to boost your productivity.

## Keyboard Shortcuts

### Working with Suggestions
- **Accept an autocomplete suggestion:** `Tab`
- **Open autocomplete suggestions:** `Ctrl + Enter`

### Working with Views (Chat, Edits, and Agent Mode)
- **Accept suggestion:** `Cmd + Enter`
- **Open inline chat:** `Cmd + I`
- **Open Copilot chats:** `Cmd + Ctrl + I`
- **Open Copilot edits:** `Cmd + Shift + I`
- **Switch between edits and agent:** `Cmd + .`

## Slash Commands (Inline and Chat)
- **Generate unit tests for the selected code:** `/tests`
- **Propose a fix for problems in the selected code:** `/fix`
- **Explain the selected code:** `/explain`
- **Start a new session (chat only):** `/clear`

## Chat Participants
Chat participants provide specialized help for context-specific tasks.

| Participant     | Description                                                                 |
|-----------------|-----------------------------------------------------------------------------|
| `#file`         | Select a file to get context-specific suggestions related to it.            |
| `#codespace`    | Find relevant code in your workspace for chat prompts. Requires `github.copilot.chat.codesearch.enabled`. |
| `@vscode`       | Offers context about Visual Studio Code commands and features.              |
| `@terminal`     | Knows about the Visual Studio Code terminal shell and its contents.         |
| `@github`       | Provides GitHub repository-related skills.                                  |

More chat participants can be found in VS Code Extensions under `tag:chat-participant`. For Azure-related help, use the `@azure` extension.

## Prompting Tips and Tricks

### Provide Context
Keep relevant files open, such as source code and data files. Add a brief description at the top of the file for better context.

### Set Appropriate Includes and References
Manually set necessary imports or module references to guide Copilot.

### Use Descriptive Naming
Meaningful variable, function, and parameter names help Copilot suggest accurate code.

### Give Examples
Include sample inputs, outputs, or implementations to guide Copilot's suggestions.

### Avoid Ambiguity
Instead of asking "What does this do?", clarify with specifics like "What does the `getWeekNumber` function do?"

### Follow Good Coding Practices
Maintain clean code, use consistent styles, and structure your code into modular components with unit tests.

### Keep History Relevant and Iterate
If the first response isn't ideal, iterate on your prompt for improved solutions.

## Custom Instructions for Copilot
To add custom instructions, create a file named `.github/copilot-instructions.md` in your repository's root. These instructions can be in Markdown format with flexible formatting options.

## GitHub Copilot in the Command Line

### CLI Commands
- **Explain a command:** `gh copilot explain "grep -rl const ."`
- **Suggest a command:** `gh copilot suggest "Undo the last commit"`

### TIP: Create a Shortcut Alias for Faster Usage

Add the following alias to your dotfiles:

```bash
alias "??"='gh copilot suggest -t shell "$@"'
```

Then you can use the `gh copilot suggest` with the following command:

```bash
?? Undo the last commit
```
